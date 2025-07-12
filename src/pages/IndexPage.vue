<template>
  <q-page class="flex">
    <div id="lpage">
      <div id="breadcrumb">
        <q-breadcrumbs class="text-brown">
          <template v-slot:separator>
            <q-icon size="1.5vw" name="chevron_right" color="primary" />
          </template>

          <q-breadcrumbs-el label="Home" icon="home" to="/" />
          <q-breadcrumbs-el label="MIKROTIK" icon="widgets" to="/" />
          <q-breadcrumbs-el label="RouterB" icon="router" to="/" />
          <q-breadcrumbs-el label="RB750" icon="broadcast_on_personal" />
        </q-breadcrumbs>
      </div>

      <div id="content">
        <div id="c-product">
          <div id="item">
            <div id="item-dg">
              <div id="ci-item">
                <q-carousel swipeable animated :autoplay="autoplay" v-model="slide" thumbnails infinite height="25vw"
                  @mouseenter="autoplay = false" @mouseleave="autoplay = true">
                  <q-carousel-slide :name="1" img-src="https://www.ds3comunicaciones.com/mikrotik/images/RB750.jpg" />
                  <q-carousel-slide :name="2"
                    img-src="https://www.ds3comunicaciones.com/mikrotik/images/RB750_top.jpg" />
                  <q-carousel-slide :name="3"
                    img-src="https://www.ds3comunicaciones.com/mikrotik/images/RB750_hand.jpg" />
                </q-carousel>
              </div>
              <div id="ci-desc">
                <div id="cid-title">
                  <h6>Router</h6>
                  <h3>RouterBOARD con 5 puertos Ethernet MIKROTIK RB750</h3>
                </div>
                <div id="cid-price">
                  <p>Precio: <span>U$ 59.00</span></p>
                  <button>
                    <img src="icons\carrito-de-compras.png" alt="">
                    <p>Comprar</p>
                  </button>
                </div>
                <div id="cid-about">
                  <p>Acerca del producto:</p>
                  <ul>
                    <li>Tipo: Router cableado SOHO</li>
                    <li>Frecuencia inalámbrica: No incluye WiFi integrado</li>
                    <li>Velocidad del CPU: 680 MHz</li>
                    <li>Memoria RAM: 32 MB</li>
                    <li>Interfaz: 5 puertos Ethernet 10/100 Mbps</li>
                    <li>Alimentación: Power Jack y PoE (10–28 V)</li>
                    <li>Consumo de energía: Máximo 2.5 W</li>
                    <li>Licencia RouterOS: Nivel 4 incluida</li>
                  </ul>

                  <a @click="visible = !visible">Ver más detalles del producto</a>
                </div>
              </div>
            </div>

            <q-slide-transition>
              <div v-show="visible">
                <div id="item-desc-g">
                  <div id="idg-1">
                    <h1>Características del Producto</h1>
                    <table border="1" cellspacing="0" cellpadding="5" bgcolor="#FFFFFF" bordercolor="#0000FF">
                      <tbody>
                        <tr>
                          <td><strong>Código del producto</strong></td>
                          <td>RB750</td>
                        </tr>
                        <tr>
                          <td><strong>Monitoreo de corriente</strong></td>
                          <td>No</td>
                        </tr>
                        <tr>
                          <td><strong>Consumo máximo de energía</strong></td>
                          <td>2.5 Watt</td>
                        </tr>
                        <tr>
                          <td><strong>Velocidad del CPU</strong></td>
                          <td>680 MHz</td>
                        </tr>
                        <tr>
                          <td><strong>RAM</strong></td>
                          <td>32 MB</td>
                        </tr>
                        <tr>
                          <td><strong>Arquitectura</strong></td>
                          <td>MIPS-BE</td>
                        </tr>
                        <tr>
                          <td><strong>Puertos LAN</strong></td>
                          <td>5</td>
                        </tr>
                        <tr>
                          <td><strong>Gigabit</strong></td>
                          <td>0</td>
                        </tr>
                        <tr>
                          <td><strong>MiniPCI</strong></td>
                          <td>0</td>
                        </tr>
                        <tr>
                          <td><strong>Wireless integrado</strong></td>
                          <td>0</td>
                        </tr>
                        <tr>
                          <td><strong>USB</strong></td>
                          <td>0</td>
                        </tr>
                        <tr>
                          <td><strong>Tarjeta de memoria</strong></td>
                          <td>0</td>
                        </tr>
                        <tr>
                          <td><strong>Power Jack</strong></td>
                          <td>10 - 28 V</td>
                        </tr>
                        <tr>
                          <td><strong>Soporte 802.3af</strong></td>
                          <td>No</td>
                        </tr>
                        <tr>
                          <td><strong>PoE</strong></td>
                          <td>10 - 28 V</td>
                        </tr>
                        <tr>
                          <td><strong>Monitor de voltaje</strong></td>
                          <td>No</td>
                        </tr>
                        <tr>
                          <td><strong>Monitor de temperatura del CPU</strong></td>
                          <td>No</td>
                        </tr>
                        <tr>
                          <td><strong>Monitor de temperatura en PCB</strong></td>
                          <td>Sí</td>
                        </tr>
                        <tr>
                          <td><strong>Dimensiones</strong></td>
                          <td>214 x 86 mm</td>
                        </tr>
                        <tr>
                          <td><strong>Rango de temperatura</strong></td>
                          <td>-40° a +55° C</td>
                        </tr>
                        <tr>
                          <td><strong>Licencia RouterOS</strong></td>
                          <td>Nivel 4</td>
                        </tr>
                      </tbody>
                    </table>


                    <p>Resultados de Rendimiento</p>
                    <table border="1" cellspacing="0" cellpadding="5" bgcolor="#FFFFFF" bordercolor="#0086C6">
                      <thead>
                        <tr bgcolor="#3366FF" style="color: #FFFFFF; font-family: Verdana;">
                          <th colspan="3"><b>Serie RB2011 @ 600 MHz (Prueba de Ethernet)</b></th>
                          <th colspan="2"><b>64 bytes</b></th>
                          <th colspan="2"><b>512 bytes</b></th>
                          <th colspan="2"><b>1518 bytes</b></th>
                        </tr>
                        <tr>
                          <th>IP Firewall</th>
                          <th>Conntrack</th>
                          <th>Modo</th>
                          <th>Mbps</th>
                          <th>Fps</th>
                          <th>Mbps</th>
                          <th>Fps</th>
                          <th>Mbps</th>
                          <th>Fps</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr>
                          <td>Off</td>
                          <td>Off</td>
                          <td>Puente</td>
                          <td>47.1</td>
                          <td>92000</td>
                          <td>358.4</td>
                          <td>87500</td>
                          <td>452.97</td>
                          <td>37300</td>
                        </tr>
                        <tr>
                          <td>On</td>
                          <td>Off</td>
                          <td>Enrutamiento</td>
                          <td>37.68</td>
                          <td>73600</td>
                          <td>294.91</td>
                          <td>72000</td>
                          <td>452.97</td>
                          <td>37300</td>
                        </tr>
                        <tr>
                          <td>On</td>
                          <td>Off</td>
                          <td>Puente</td>
                          <td>35.48</td>
                          <td>69300</td>
                          <td>230.2</td>
                          <td>56200</td>
                          <td>446.9</td>
                          <td>36800</td>
                        </tr>
                        <tr>
                          <td>On</td>
                          <td>On</td>
                          <td>Enrutamiento</td>
                          <td>28.42</td>
                          <td>55500</td>
                          <td>222.41</td>
                          <td>54300</td>
                          <td>445.68</td>
                          <td>36700</td>
                        </tr>
                        <tr>
                          <td>On</td>
                          <td>On</td>
                          <td>Puente</td>
                          <td>18.94</td>
                          <td>37000</td>
                          <td>149.5</td>
                          <td>36500</td>
                          <td>425.04</td>
                          <td>35000</td>
                        </tr>
                      </tbody>
                    </table>

                  </div>
                  <div id="idg-2">
                    <h1>Descripción del producto</h1>

                    <h2>Desempeño Superior</h2>

                    <p>
                      El RouterBOARD MIKROTIK RB750 es un pequeï¿½o router que viene con cinco puertos Ethernet, en una
                      caja
                      de
                      plástico.

                      De diseño atractivo todo lo que buscan en una unidad pequeña SOHO, su precio es menor que la
                      licencia
                      RouterOS, es perfecto para administrar su red de cable en casa, el RB750 lo tiene todo.

                      No solo es económico, es pequeña y fácil de usar. Es probable que sea router MPLS más
                      económico
                      en el mercado. No hay compromiso entre el precio y características el RB750 tiene ambas cosas. Con
                      su
                      diseño compacto y un aspecto limpio, se ajustará perfectamente a su entorno SOHO.
                    </p>


                    <h2>Aplicaciones</h2>
                    <ul>
                      <li>Interconecte sucursales y oficinas de empresas públicas y privadas(Wireless LAN).
                      </li>
                      <li>Provee servicios de internet inalámbrico.</li>
                      <li>(ISP inalámbrico).</li>
                      <li>Sistemas WiFi.</li>
                    </ul>

                    <h2>Ventajas</h2>
                    <ul>
                      <li>Pequeño y compacto.</li>
                      <li>Caja de plástico blanca.</li>
                      <li>Cinco puertos Ethernet.</li>
                      <li>Increíblemente rápido.</li>
                    </ul>
                  </div>

                  <div id="idg-3">
                    <p>Descargar: </p>

                    <button>Ficha Técnica</button>
                    <button>Manual</button>
                    <button>Especificaciones</button>
                  </div>
                </div>
              </div>
            </q-slide-transition>
          </div>
          <div id="recomendaciones">
            <div class="q-pa-md" id="rd-1" style="max-width: 100%">
              <q-list padding bordered class="rounded-borders">
                <q-expansion-item dense dense-toggle expand-separator icon="add_task" label="Nuestras Marcas">
                  <div id="r-marcas">
                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/ALFA_logo1.gif" alt="Alfa">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/airlivelogo.gif" alt="Airlive">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/andrew/images/logo_andrew.jpg" alt="Andrew">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/amp_logo2-91x20.jpg" alt="AMP">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/amphenol_logo-100x21.jpg" alt="Amphenol">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/Belden-Logo-93x15.jpg" alt="Belden">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/cisco/images/logo-cisco.gif" alt="Cisco">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/dahua/images/dahua_logo.jpg" alt="Dahua">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/D-Link_Logo-100x26.jpg" alt="D-Link">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/dixon_logo-100x19.jpg" alt="Dixon">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/FibreFab/images/logo_fibrefab.png" alt="FibreFab">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/lanpro/images/lanpro_logo.jpg" alt="LanPro">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/sitebuilder/images/lcom_logo-100x23.jpg" alt="L-Com">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/mikrotik_logo-100x24.png" alt="MikroTik">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/panduit/images/panduit_logo.jpg" alt="Panduit">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/satra/images/satra.JPG" alt="Satra">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/siemon/images/siemon_logo1.GIF" alt="Siemon">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/tp-link_logo-100x13.jpg" alt="TP-Link">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/trendnet_logo-100x20.jpg" alt="Trendnet">
                    </a>

                    <a href="#">
                      <img src="http://www.ds3comunicaciones.com/belden/images/ubnt_logo-100x47.png" alt="Ubiquiti">
                    </a>

                  </div>
                </q-expansion-item>

                <q-expansion-item dense dense-toggle expand-separator icon="signal_wifi_off" label="Lista de Precios">
                  <div id="r-price">
                    <a href="#">Lista de precios AMP</a>
                    <a href="#">Lista de precios Amphenol</a>
                    <a href="#">Lista de precios Andrew</a>
                    <a href="#">Lista de precios APC</a>
                    <a href="#">Lista de precios CISCO</a>
                    <a href="#">Lista de precios D-Link</a>
                    <a href="#">Lista de precios Dixon</a>
                    <a href="#">Lista de precios Energit</a>
                    <a href="#">Lista de precios Fibra</a>
                    <a href="#">Lista de precios HP</a>
                    <a href="#">Lista de precios Mikrotik</a>
                    <a href="#">Lista de precios Nexxt Solutions</a>
                    <a href="#">Lista de precios Panduit</a>
                    <a href="#">Lista de precios Siemon</a>
                    <a href="#">Lista de precios Teldor</a>
                    <a href="#">Lista de precios TRENDnet</a>
                    <a href="#">Lista de precios Ubiquiti</a>

                  </div>
                </q-expansion-item>


              </q-list>
            </div>

          </div>
        </div>

        <div id="ci-adicionales">
          <p>Productos que podrían interesarte: </p>

          <div id="cia-car">
            <q-carousel v-model="slide" transition-prev="slide-right" transition-next="slide-left" swipeable animated
              control-color="amber" navigation padding arrows height="auto" class=" rounded-borders">
              <q-carousel-slide :name="1" class="column no-wrap">

                <div id="ciac-order">
                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1100</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1200.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1200</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB2011L-IN-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 5 puertos Gigabit Ethernet MIKROTIK RB2011L-IN</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AH-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AH</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AHx2-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AHx2</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>
                </div>



              </q-carousel-slide>
              <q-carousel-slide :name="2" class="column no-wrap">

                <div id="ciac-order">
                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1100</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1200.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1200</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB2011L-IN-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 5 puertos Gigabit Ethernet MIKROTIK RB2011L-IN</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AH-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AH</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AHx2-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AHx2</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>
                </div>



              </q-carousel-slide>
              <q-carousel-slide :name="3" class="column no-wrap">

                <div id="ciac-order">
                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1100</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1200.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1200</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB2011L-IN-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 5 puertos Gigabit Ethernet MIKROTIK RB2011L-IN</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AH-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AH</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AHx2-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AHx2</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>
                </div>



              </q-carousel-slide>
              <q-carousel-slide :name="4" class="column no-wrap">

                <div id="ciac-order">
                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1100</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1200.jpg">

                    <q-card-section>
                      <div class="text-h6">ROUTERBOARD MIKROTIK RB1200</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB2011L-IN-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 5 puertos Gigabit Ethernet MIKROTIK RB2011L-IN</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AH-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AH</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>

                  <q-card class="my-card">
                    <img src="https://www.ds3comunicaciones.com/mikrotik/images/RB1100AHx2-1.png">

                    <q-card-section>
                      <div class="text-h6">RouterBOARD con 13 puertos Gigabit Ethernet MIKROTIK RB1100AHx2</div>
                    </q-card-section>

                    <q-card-actions>
                      <q-btn flat color="primary" label="Ver Producto" />
                    </q-card-actions>
                  </q-card>
                </div>



              </q-carousel-slide>


            </q-carousel>
          </div>
        </div>
      </div>

    </div>

    <footer>
      <div id="ff">
        <div class="f-col1">
          <img src="logos\Logo1.jpg" alt="">
          <p class="fc1-t">Redes Sociales</p>
          <div class="fc1-i">
            <a href=""><img src="icons\facebook.png" alt=""></a>
            <a href=""><img src="icons\whatsapp.png" alt=""></a>
          </div>
          <p class="fc1-t">Correo</p>
          <a href="#">
            <img src="icons\correo.png" alt="">
            <p>netperu100@hotmail.com</p>
          </a>
        </div>

        <div class="f-col2">
          <h2 class="fc2-t">Soluciones</h2>
          <a href="#">Access Point</a>
          <a href="#">Antenas MIMO</a>
          <a href="#">Antenas de Panel</a>
          <a href="#">Antenas Sectoriales</a>
          <a href="#">Cable Pigtail</a>
          <a href="#">Media Converter</a>
        </div>

        <div class="f-col3">
          <h2 class="fc2-t">Soluciones</h2>
          <a href="#">Soporte Técnico</a>
          <a href="#">Acerca de Nosotros</a>
        </div>

        <div class="f-col4">
          <h2 class="fc2-t">Contacto</h2>
          <a href="#">
            <img src="icons\Télefono.ico" alt="">
            <p>994 428 965</p>
          </a>
          <a href="#">
            <img src="icons\Télefono.ico" alt="">
            <p>996 533 223</p>
          </a>

          <h2 class="fc2-t">Horario de Atención</h2>
          <p>Lunes a Viernes: 9:00 - 18:00</p>
          <p>Sábados: 9:00 - 13:00</p>
        </div>
      </div>
    </footer>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      slide: 1,
      visible: false,
      autoplay: true
    };
  }
});
</script>


<style lang="scss" scoped>
#lpage {
  flex-grow: 1;
  padding: 0.5vw 4vw;

  #breadcrumb {
    font-size: 0.75vw;
    padding: 0.5vw 0;
  }

  #content {

    #c-product {
      box-shadow: 0 4px 10px 0 rgba(0, 0, 0, .1);
      border-radius: 0.5vw;
      padding: 1vw;
      display: grid;
      grid-template-columns: 75% 25%;

      #item {
        grid-column-start: 1;
        grid-column-end: 2;

        #item-dg {
          display: grid;
          grid-template-columns: 60% 40%;

          #ci-item {
            grid-column-start: 1;
            grid-column-end: 2;
            overflow: hidden;
          }

          #ci-desc {
            grid-column-start: 2;
            grid-column-end: 3;
            padding: 1vw;

            #cid-title {
              h6 {
                padding: 0;
                margin: 0;
                opacity: 0.6;
              }

              h3 {
                padding: 0%;
                margin: 0;
                font-size: 1.5vw;
                font-weight: bold;
                opacity: 0.6;
              }
            }

            #cid-price {
              display: flex;
              flex-direction: row;
              justify-content: space-between;
              align-items: center;
              margin: 1vw 3vw 1vw 0;
              // border: 1px solid red;
              padding: 1vw 0;
              border-top: 0.1vw solid rgba(128, 128, 128, 0.5);
              border-bottom: 0.1vw solid rgba(128, 128, 128, 0.5);

              p {
                all: unset;
                font-size: 1.5vw;
                font-weight: bold;

                span {
                  color: red;
                }
              }

              button {
                font-size: 0.75vw;
                padding: 0.5vw;
                display: flex;
                flex-direction: row;
                gap: 1vw;
                justify-items: center;
                align-items: center;
                border-radius: 1vw;
                background-color: $primary;
                border: none;
                cursor: pointer;
                transition: all 0.2s;

                img {
                  width: 1.5vw;
                  filter: invert(1);
                }

                p {
                  color: white;
                }

                &:hover {
                  background-color: $secondary;
                  transform: scale(1.1);
                }
              }
            }

            #cid-about {
              p {
                margin: 0;
                padding: 0;
                font-weight: bold;
                font-size: 1vw;
              }

              ul {
                margin: 0;
                margin-top: 0.5vw;
                margin-bottom: 0.5vw;

                li {
                  font-size: 0.75vw;
                }
              }

              a {
                padding: 1vw;
                font-size: 1.25vw;
                letter-spacing: 0.05vw;
                text-decoration: underline;
                font-weight: bold;
                cursor: pointer;
                transition: 0.2s all;

                &:hover {
                  color: blue;
                }
              }
            }
          }
        }

        #item-desc-g {
          display: grid;
          grid-template-columns: 50% 50%;
          grid-template-rows: auto auto;
          margin-top: 2vw;

          p {
            font-size: 1.5vw;
            width: 100%;
            margin: 0;
            padding: 0;
          }

          h1 {
            display: flex;
            justify-self: center;
            font-size: 2vw;
            align-self: center;
            font-weight: bold;
          }


          #idg-1 {
            grid-column-start: 1;
            grid-column-end: 2;
            grid-row-start: 1;
            grid-row-end: 2;
            display: flex;
            flex-direction: column;
            gap: 2vw;
            align-content: center;
            align-items: center;
            // border: 1px solid red;
            font-size: 0.75vw;

            p {
              border-bottom: 0.25vw rgba(128, 128, 128, 0.5);
            }


            #idg-st {
              font-weight: bold;
              // border: 1px solid red;
            }

            table {
              width: 30vw;
            }
          }

          #idg-2 {
            grid-column-start: 2;
            grid-column-end: 3;
            grid-row-start: 1;
            grid-row-end: 2;
            padding: 0 2vw;


            h2 {
              font-weight: bold;
              opacity: 0.6;
              font-size: 1.5vw;
            }

            p,
            li {
              font-size: 1vw;
            }


          }

          #idg-3 {
            grid-column-start: 1;
            grid-column-end: 3;
            grid-row-start: 2;
            grid-row-end: 3;
            // border: 1px solid red;
            margin-top: 2vw;
            padding: 1vw;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            justify-items: center;

            gap: 2vw;

            p {
              all: unset;
              font-size: 1.5vw;
              font-weight: bold;
              opacity: 0.6;
            }

            button {
              background-color: $secondary;
              border-radius: 2vw;
              font-size: 1.5vw;
              font-weight: bold;
              padding: 0.5vw 2vw;
              border: none;
              transition: 0.2s all;
              color: white;
              cursor: pointer;

              &:hover {
                background-color: $primary;
              }
            }
          }

        }

      }

      #recomendaciones {
        grid-column-start: 2;
        grid-column-end: 3;
        font-size: 1.5vw;
        font-weight: bold;

        #r-marcas {
          display: flex;
          flex-direction: column;
          gap: 0.05vw;
          align-items: center;
          width: 100%;
          padding: 1vw;

          a {
            img {
              width: 7.5vw;
            }
          }
        }

        #r-price {
          display: flex;
          flex-direction: column;
          padding: 1vw;

          a {
            font-size: 1vw;
            width: 100%;
            font-weight: normal;
            color: $primary;
            transition: 0.2s all;

            &:hover {
              color: $primary;
              background-color: rgba($primary, 0.2);
            }
          }
        }
      }
    }

    #ci-adicionales {
      p {
        margin-top: 2vw;
        margin-bottom: 0.5vw;
        font-size: 1vw;
        font-weight: bold;
        opacity: 0.6;
      }

      #cia-car {
        box-shadow: 0 4px 10px 0 rgba(0, 0, 0, .1);
        border-radius: 0.5vw;
        padding: 1vw;


        #ciac-order {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          gap: 1vw;

          .my-card {
            width: 15vw;
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            img {
              height: 5vw;
            }
          }
        }
      }
    }
  }

}

footer {
  display: flex;
  flex-direction: column;
  padding: 1vw 4vw;
  width: 100%;

  #ff {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;

    .f-col1 {
      img {
        width: 10vw;
        margin-bottom: 1vw;
      }

      p {
        font-size: 1vw;
        font-weight: bold;
        opacity: 0.6;
      }

      .fc1-i {
        display: flex;
        flex-direction: row;
        gap: 1vw;
        margin-bottom: 1vw;
      }

      a {
        display: flex;
        flex-direction: row;
        text-decoration: none;
        gap: 1vw;
        align-items: start;
        justify-content: start;
        color: black;

        img {
          width: 1.5vw;
          height: auto;
        }
      }
    }

    .f-col2 {
      display: flex;
      flex-direction: column;
      gap: 0.5vw;

      a {
        font-size: 0.9vw;
        text-decoration: none;
        color: black;
        width: 10vw;
        padding: 0.1vw;

        &:hover {
          text-decoration: underline;
          background-color: rgba($primary, 0.2);
          color: $primary;
        }
      }

    }

    .fc2-t {
      font-size: 1vw;
      font-weight: bold;
      opacity: 0.6;
      margin-bottom: 0vw;
    }

    .f-col3 {
      display: flex;
      flex-direction: column;

      gap: 0.5vw;

      a {
        font-size: 0.9vw;
        text-decoration: none;
        color: black;
        width: 10vw;
        padding: 0.1vw;

        &:hover {
          text-decoration: underline;
          background-color: rgba($primary, 0.2);
          color: $primary;
        }
      }
    }

    .f-col4 {
      display: flex;
      flex-direction: column;
      gap: 0.5vw;

      a {
        display: flex;
        flex-direction: row;
        font-size: 0.9vw;
        text-decoration: none;
        color: black;
        width: 10vw;
        padding: 0.1vw;
        gap: 0.5vw;

        img {
          width: 1vw;
        }

        &:hover {
          text-decoration: underline;
          background-color: rgba($primary, 0.2);
          color: $primary;
        }
      }

      p {
        font-size: 0.75vw;
        text-decoration: none;
        color: black;
        width: 10vw;
        margin: 0;
        padding: 0;
      }
    }
  }
}
</style>
