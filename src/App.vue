<template>
  <div class="all" style="height: 100vh;">


    <!DOCTYPE html>
    <html lang="en">

    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
      <title>CAR - Travis</title>
      <meta name="description" content="CAR BY TRAVIS" />

      <!-- Favicon -->
      <link rel="shortcut icon" href="https://car.travis.ro/log-CAR.png">
      <link rel="icon" href="https://car.travis.ro/log-CAR.png" type="image/x-icon">

      <!-- vector map CSS -->
      <link href="vendors/vectormap/jquery-jvectormap-2.0.3.css" rel="stylesheet" type="text/css" />

      <!-- Toggles CSS -->
      <link href="vendors/jquery-toggles/css/toggles.css" rel="stylesheet" type="text/css">
      <link href="vendors/jquery-toggles/css/themes/toggles-light.css" rel="stylesheet" type="text/css">

      <!-- Toastr CSS -->
      <link href="vendors/jquery-toast-plugin/dist/jquery.toast.min.css" rel="stylesheet" type="text/css">

      <!-- switchery -->
      <link href="vendors/switchery/dist/switchery.min.css" rel="stylesheet" type="text/css">

      <!-- Custom CSS -->
      <link href="dist/css/style.css" rel="stylesheet" type="text/css">

      <!-- jquery ui -->

      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jqueryui/1.12.1/jquery-ui.min.css"
        integrity="sha512-aOG0c6nPNzGk+5zjwyJaoRUgCdOrfSDhmMID2u4+OIslr0GjpLKo7Xm0Ao3xmpM4T8AmIouRkqwj1nrdVsLKEQ=="
        crossorigin="anonymous" referrerpolicy="no-referrer" />

        <link rel="stylesheet" href="style.css">

    
    </head>

    <body>

      <div class="hk-wrapper hk-vertical-nav">

        <form role="search" class="navbar-search">
          <div class="position-relative">
            <a href="javascript:void(0);" class="navbar-search-icon"><span class="feather-icon"><i
                  data-feather="search"></i></span></a>
            <input type="text" name="example-input1-group2" class="form-control" placeholder="Cauta in CAR...">
            <a id="navbar_search_close" class="navbar-search-close" href="#"><span class="feather-icon"><i
                  data-feather="x"></i></span></a>
          </div>
        </form>

                  <!-- Breadcrumb -->
                  <nav class="hk-breadcrumb" aria-label="breadcrumb">
                    <ol class="breadcrumb breadcrumb-light bg-transparent" style="direction: rtl;">
                      <div class="icon-container">
                    <li>
                        <ul class="icons-list" style="color: #000; margin-right: 20px; direction: ltr; margin-left: 10px; margin-right: 10px;">
                            <li class="dropdown">
                                <a href="#" class="dropdown-toggle" data-toggle="dropdown"><i class="fa fa-at" style="color: #000; font-size: 35px;"></i></a>
                                <ul class="dropdown-menu dropdown-menu-right" style="color: #000;">
                                    <li>Client</li>
                                    <li>
                                        <a style="color: #000 !important;" target="_blank" href="https://car.travis.ro/?pag=rezervari&pag2=trimite-email&tip=client&ide=6&rezervare=102420">
                                            <i class="fa fa-at "></i>Email confirmare
                                        </a>
                                    </li>
                                    <li>
                                        <a style="color: #000 !important;" target="_blank" href="https://car.travis.ro/?pag=rezervari&pag2=trimite-email&tip=client&ide=7&rezervare=102420">
                                            <i class="fa fa-at "></i>Email anulare
                                        </a>
                                    </li>
                                    <li>Furnizor</li>
                                    <li>
                                        <a style="color: #000 !important;" target="_blank" href="https://car.travis.ro/?pag=rezervari&pag2=trimite-email&tip=furnizor&ide=8&rezervare=102420">
                                            <i class="fa fa-at "></i>Email comanda
                                        </a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </li>
                    <li>
                        <select id="status" name="status" class="form-control" style="direction: ltr; margin-bottom: 0px !important;">
                            <option value="confirmed2">Confirmata - fara plata</option>
                            <option value="confirmed3">Confirmata - cu plata</option>
                            <option value="confirmed">Finalizata</option>
                            <option value="retrasa">Retrasa</option>
                            <option value="pending">In asteptare (furnizor)</option>
                            <option value="transfer">Transfer</option>
                            <option value="termen_lung">Termen lung</option>
                            <option value="review">Decontat</option>
                            <option value="anulat">Anulata</option>
                        </select>
                    </li>
                    <li>
                        <div class="icon_pending" style="width: 200px; height: 40px; margin-top: 0; margin-left: 10px; margin-right: 10px; background-color: yellow;"></div>
                    </li>
                </div>


                      <div class="btn-container">
                          <li>
                              <a id="btn2" href="?pag=rezervari&pag2=printeaza&idr=102420" target="_blank" class="btn btn-primary btn-labeled btn-labeled-right bg-blue heading-btn">
                                  <i class="fa fa-print"></i> Printeaza
                              </a>
                          </li>
                          <li>
                              <a id="btn1" href="?pag=rezervari" class="btn btn-primary btn-labeled btn-labeled-right bg-blue heading-btn" style="margin-right: 10px;">
                                  Afiseaza rezervari
                              </a>
                          </li>
                          <li>
                              <a id="butLinkUnic" data-toggle="modal" data-target="#modalLinkUnic" class="btn btn-primary btn-labeled btn-labeled-right bg-blue heading-btn" style="margin-right: 10px; color: #fff;">
                                  Link TASK
                              </a>
                          </li>
                      </div>

                    </ol>
                  </nav>


        <!-- Page container -->
        <div class="hk-pg-wrapper">

          <!-- Page container -->
          <div class="container">

            <!-- Page content -->
            <div class="hk-sec-wrapper" style=" margin-top: -40px;">

              <!-- Main content -->
              <div class="content-wrapper">
                <div id="app">
                  <!-- message test -->

                  <h3 id="reservationInfo" style="text-align: center;">
                      Rezervarea #
                      <input id="idr" type="text" value="43022" style="width: 110px;" />
                      <a href="#" id="okidr" class="btn btn-primary">Ok</a>
                      <br /> <br />

                      <div class="info-text" id="reservationDetails">
                          Rezervare facuta de client: test test - <span style="color: #5A5A5A;">Site: rentacar.travis.ro</span>
                      </div>

                      <div class="info-text" id="reservationDetails">
                          <div>La data de 29.03.2024 16:09</div>
                          <div>Mod plata: modalitate plata</div>
                          <div>Status plata: status plata</div>
                      </div>
                  </h3>


                  <div class="row">
                    <div class="col-md-12 col-sm-12">
                      <hr />
                    </div>
                  </div>


                  <div class="row">
                    <div class="col-md-4 col-sm-12" data-category="detalii-inchiriere">
                      <h4>Detalii inchiriere </h4>
                      <h6 style="margin-top: 15px;">Predare:</h6>

                      <input type="date" class="form-control datepicker" id="data1" name="data1" />
                      <input type="time" class="form-control" id="ora1" name="ora1" />
                      <select id="locatie1" name="locatie1" class="form-control">
                          <option disabled value="">Please select one</option>
                      </select>


                      <table style="width: 100%; border: 0;">
                          <tr>
                              <td style="width: 90%;">
                                  <select class="form-control" name="id_driver_out" id="id_driver_out">
                                      <option value="">Sofer predare</option>
                                  </select>
                              </td>
                              <td>
                                  <div title="Sofer nealocat sau soferul inca nu a raspuns!" style="text-align:center;"><i
                                          class="fa fa-question" style="font-size: 20px; color: orange; font-weight: bold;"></i>
                                  </div>
                              </td>
                          </tr>
                      </table>


                      sergiu hriscu a inceput procedura de predare dar nu a finalizat!<br /> Km. predare: <input
                      type="text" id="km_predare_new" value="1" class="form-control"
                      style="width: 80px; display:inline;" /> <a
                      href="https://car.travis.ro/view_task_img.php?url=https://task.travis.ro/alfota/pdkm_1711721734_.txt"
                      target="_blank">Deschide foto</a> <a href="#" id="adauga-foto-km-but-predare">Adauga foto km</a>
                      <br />
                      <div id="foto-km-predare" style="display: none;">
                          <label>Foto km predare</label>
                          <input type="file" id="foto-km-predare-file" class="form-control" style="width: 100%;"
                              onchange="foto_km('predare');" />

                          <a id="saveFotoPredare"
                              style="cursor:pointer; background-color: orange; color: #fff; padding: 10px;">Salveaza
                              foto</a>
                      </div>
                      <br />

                      <h6 style="margin-top: 15px;">Preluare:</h6>

                      <input type="date" class="form-control datepicker" id="data2" name="data2" />
                        <input type="time" class="form-control" id="ora2" name="ora2" />
                        <select id="locatie2" name="locatie2" class="form-control">
                            <option disabled value="">Please select one</option>
                        </select>

                        <table style="width: 100%; border: 0;">
                            <tr>
                                <td style="width: 90%;">
                                    <select class="form-control" name="id_driver_in" id="id_driver_in">
                                        <option value="">Sofer preluare</option>
                                    </select>
                                </td>
                                <td>
                                    <div title="Sofer nealocat sau soferul inca nu a raspuns!" style="text-align:center;"><i
                                            class="fa fa-question" style="font-size: 20px; color: orange; font-weight: bold;"></i>
                                    </div>
                                </td>
                            </tr>
                        </table>





                      <div id="foto-km-preluare" style="display: none;">
                        <label>Foto km preluare</label>
                        <input type="file" id="foto-km-preluare-file" class="form-control" style="width: 100%;"
                          onchange="foto_km('preluare');" />

                        <a id="saveFotoPreluare"
                          style="cursor:pointer; background-color: orange; color: #fff; padding: 10px;">Salveaza
                          foto</a>
                      </div>


                      <br />

                      <span style="font-size: 17px; color: green; font-weight:bold;"> zileRent zile
                        inchiriere</span> <span id="zile_rent_preview"
                        style="font-size: 17px; color: green; font-weight:bold;"></span>

                      <br /> <span style="font-size: 20px;"> <input type="checkbox" id="over_oferta" /> Afiseaza conform
                        oferta / contract [fara pret]</span>



                    </div>

                    <div class="col-md-4 col-sm-12" data-category="detalii-auto">

                      <h4 style="margin-bottom: 15px;">Detalii auto </h4>
                      <h5 id="spatiu-sub-detalii-auto">&nbsp;</h5>
                      <select name="auto" class="form-control auto_select" id="auto">
                          <option disabled value="">Please select one</option>
                      </select>

                      <select name="auto_fizic" class="form-control" id="auto_fizic">
                      </select>

                      <h5 style="display: block;">&nbsp;</h5>



                      <ul id="incluse_preview"
                        style="list-style-type: circle !important; padding-left: 20px; font-size: 12px;">
                        <li><b>Furnizor:</b> furnizor <span style="color:red;"> societate</span></li>
                        <li><b>Locatie auto:</b> <span id="locatieauto">locatie auto</span></li>
                        <li>garantie </li>
                        <li><span style="color: red;">cash</span>&nbsp; <a
                            href="https://car.travis.ro/view_task_img.php?url=https://task.travis.ro/alfota/pdgar_1711721774_.txt"
                            target="_blank">Deschide foto</a></li>
                        <li><input type="text" id="over_garantie" placeholder="Garantie manual" class="form-control"
                            style="width: 120px;" value="" /></li>
                        <li>Nr.km.: nrKm <span id="nrkm_preview"></span></li>
                        <li>Kilometri nelimitati!<span id="nrkm_preview"></span></li>
                        <li><input type="text" placeholder="Km manual" id="over_km" class="form-control"
                            style="width: 120px;" value="" /></li>


                        <!--  <li v-if="tarifDislocare > 0">Dislocare preluare {{ locatie1 }} {{ tarifDislocare }} &euro;</li>
                        <li v-if="tarifDislocare2 > 0">Dislocare predare {{ locatie2 }} {{ tarifDislocare2 }} &euro;</li>
                        <li v-if="tarifHours > 0">ExtraHours {{ tarifHours }} &euro;</li> -->
                      </ul>
                    </div>

                    <div class="col-md-4 col-sm-12" data-category="servicii-suplimentare">
                      <h4 style="margin-bottom: 15px;">Servicii suplimentare</h4>
                      <h5 id="spatiu-sub-detalii-auto-2">&nbsp;</h5>

                      <ul id="extraoptiuni_preview"
                        style="list-style-type: circle !important; padding-left: 20px; font-size: 14px;">
                        <li>
                          suplimentar
                        </li>
                      </ul>

                      <h5 style="margin-top: 15px;">
                        Informatii/Solicitari speciale</h5>
                      <span>Solicitari speciale: solicitari speciale
                        <br /></span>
                      <span>Nr zbor: nrZbor <br /></span>

                    </div>

                    <div class="col-md-8 col-sm-12">
                      <br />
                      <a id="preview-disponibilitate" class="btn btn-primary"
                        style=" cursor: pointer; width: 100%; background-color: blue; color: #fff; border-color: blue; text-transform: uppercase; font-weight:bold;">Verifica
                        disponibilitate</a>

                    </div>



                  </div>

                  <div class="row">
                    <div class="col-md-12 col-sm-12">
                      <hr />
                    </div>
                  </div>

                  <div class="row">
                    <div class="col-md-12 col-sm-12">
                      <input type="hidden" name="id_decont" value="9794" /><input type="hidden"
                        name="comison_inchiriere" value="0.04" /><input type="hidden" name="comision_protectii"
                        value="0.3" />
                      <h4>Detalii financiare</h4>

                      <table style="width: 100%;" data-category="tip-tarif">
                      <tr>
                          <td colspan="3">
                              <input type="hidden" name="tiptarifprev" id="tiptarifprev" />
                              <select name="tip_tarif" id="tip_tarif" class="form-control date_importante">
                                  <option value="1">Tarif Standard</option>
                                  <option>Tarif Budget</option>
                                  <option>Tarif Plus</option>
                              </select>
                          </td>
                      </tr>
                      <tr>
                          <td colspan="5">Cheltuieli</td>
                      </tr>
                  </table>

                      <table style="width: 100%; margin-bottom: 50px;" data-category="decont">

                        <tr>
                          <td class="stil_coloana_discount_detalii">inchiriere</td>
                          <td>
                            <input type="text" name="inchiriere" id="inchiriere" value="140"
                              class="form-control date_importante input_decont" />
                          </td>

                          <td><span id="tarifbaza_preview"></span></td>
                          <td></td>
                          <td></td>
                          <td></td>
                          <td></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii">reducere <span id="reducere_cod"></span></td>
                          <td><input type="text" name="reducere" id="reducere" value="0"
                              class="form-control date_importante input_decont" /></td>
                          <td><span id="reducere_preview"></span> <span id="reducere_nume_preview"
                              style="font-size: 12px;"></span></td>
                          <td></td>
                          <td></td>
                          <td>brut</td>
                          <td>agent</td>
                          <td>impozit</td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii stil_coloana_bold">total inchiriere</td>
                          <td><input type="text" name="total_inchiriere" id="total_inchiriere"
                              class="form-control date_importante input_decont" value="140" /></td>
                          <td><span id="total_inchiriere_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">
                            comision agent inchiriere

                          </td>
                          <td>
                            <select name="agent_inchiriere_id" id="agent_inchiriere" class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select>
                          </td>
                          <td><input type="text" name="agent_inchiriere_comision" id="agent_inchiriere_comision"
                              class="form-control  input_decont" value="0" /></td>
                          <td>
                            <span id="comision_agent_inchiriere">0</span>
                          </td>
                          <td><span id="impozit_agent_inchiriere">0</span></td>
                        </tr>


                        <tr>
                          <td class="stil_coloana_discount_detalii">protectie</td>
                          <td><input type="text" name="protectii" id="protectii"
                              class="form-control date_importante input_decont" value="0" /></td>
                          <td><span id="protectie_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">comision agent protectie</td>
                          <td> <select name="agent_protectie_id" id="agent_protectie"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select></td>
                          <td><input type="text" name="agent_protectie_comision" id="agent_protectie_comision"
                              class="form-control input_decont" value=0 /></td>
                          <td><span id="comision_agent_protectie">0</span></td>
                          <td><span id="impozit_agent_protectie">0</span></td>
                        </tr>



                        <tr>
                          <td colpan="8"></td>
                        </tr>



                        <tr>
                          <td class="stil_coloana_discount_detalii">extra hours predare catre client
                            <div style="display:none;">
                              <span id="extrahours">tarif extra hours</span>
                              <span id="extrahours_preview"></span>
                            </div>
                          </td>
                          <td><input type="text" name="extrahours_preluare_incasari" id="extrahours_preluare_incasari"
                              class="form-control date_importante input_decont" value="0" /></td>
                          <td><span id="extrahours_preluare_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">extra hours predare catre client</td>
                          <td> <select name="agent_extrahours_predare" id="agent_extrahours_predare"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select></td>
                          <td><input type="text" name="extrahours_predare_cheltuieli" id="extrahours_predare_cheltuieli"
                              class="form-control input_decont" value="0" /></td>
                          <td><input type="text" name="info_extra_predare" id="info_extra_predare" value=""
                              class="form-control select_decont" placeholder="info" /></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii">extra hours preluare de la client</td>
                          <td><input type="text" name="extrahours_predare_incasari" id="extrahours_predare_incasari"
                              class="form-control date_importante input_decont" value="0" /></td>
                          <td><span id="extrahours_predare_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">extra hours preluare de la client</td>
                          <td> <select name="agent_extrahours_preluare" id="agent_extrahours_preluare"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select></td>
                          <td><input type="text" name="extrahours_preluare_cheltuieli"
                              id="extrahours_preluare_cheltuieli" class="form-control  input_decont" value="0" /></td>

                          <td><input type="text" name="info_extra_preluare" id="info_extra_preluare" value=""
                              class="form-control select_decont" placeholder="info" /></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii">
                            dislocare predare <br />
                            <span id="locatie_preluare" style="display:none;">Iasi</span>
                          </td>
                          <td><input type="text" name="dislocare_preluare_incasari" id="dislocare_preluare_incasari"
                              class="form-control input_decont" value="0" /></td>
                          <td><span id="dislocare1_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">dislocare predare (decont/OD)</td>
                          <td>

                            <input name="od_predare" id="od_predare" type="text" value="" placeholder="numar decont/OD"
                              class="form-control select_decont" />
                            <select name="agent_dislocare_predare" id="agent_dislocare_predare"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select>
                          </td>
                          <td><input type="text" name="dislocare_predare_cheltuieli" id="dislocare_predare_cheltuieli"
                              class="form-control input_decont" value="0" /></td>

                          <td><input type="text" name="info_dislocare_predare" id="info_dislocare_predare" value=""
                              class="form-control select_decont" placeholder="info" /></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii">dislocare preluare <br /> <span id="locatie_predare"
                              style="display:none;">Iasi</span></td>
                          <td><input type="text" name="dislocare_predare_incasari" id="dislocare_predare_incasari"
                              class="form-control date_importante input_decont" value="0" /></td>
                          <td><span id="dislocare2_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">dislocare preluare (decont/OD)</td>
                          <td>
                            <input name="od_preluare" id="od_preluare" type="text" value=""
                              placeholder="numar decont/OD" class="form-control select_decont" />
                            <select name="agent_dislocare_preluare" id="agent_dislocare_preluare"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select>
                          </td>
                          <td><input type="text" name="dislocare_preluare_cheltuieli" id="dislocare_preluare_cheltuieli"
                              class="form-control input_decont" value="0" /></td>

                          <td><input type="text" name="info_dislocare_preluare" id="info_dislocare_preluare" value=""
                              class="form-control select_decont" placeholder="info" /></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii">servicii suplimentare</td>
                          <td><input type="text" name="servicii_suplimentare_incasari"
                              id="servicii_suplimentare_incasari" class="form-control date_importante input_decont"
                              value="0" /></td>
                          <td><span id="suplimentare_preview"></span></td>
                          <td class="stil_coloana_discount_detalii">alte cheltuieli</td>
                          <td> <select name="operator_alte_cheltuieli_1" id="operator_alte_cheltuieli_1"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select></td>
                          <td><input type="text" name="alte_cheltuieli_suma1" id="alte_cheltuieli_suma1" value="0"
                              class="form-control input_decont" placeholder="suma" /></td>

                          <td><input type="text" name="alte_cheltuieli_detalii1" id="alte_cheltuieli_detalii1" value=""
                              class="form-control select_decont" placeholder="info" /></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td class="stil_coloana_discount_detalii">alte incasari<br />
                            <input type="text" placeholder="detalii incasari" name="alte_incasari_detalii"
                              id="alte_incasari_detalii" value="" class="form control select_decont" />
                          </td>
                          <td><input type="text" name="alte_incasari" id="alte_incasari" value="0"
                              class="form-control input_decont" /></td>
                          <td> </td>
                          <td class="stil_coloana_discount_detalii">alte cheltuieli</td>
                          <td><select name="operator_alte_cheltuieli_2" id="operator_alte_cheltuieli_2"
                              class="form-control select_decont">
                              <option value="0">-</option>
                              <option value="2">adrian</option>
                              <option value="98">alexgalben</option>
                              <option value="97">alexandru.galan</option>
                              <option value="26">andrei.ciuta</option>
                              <option value="108">andrei.radu</option>
                              <option value="101">andrei.sofron</option>
                              <option value="17">andrei.zamosteanu</option>
                              <option value="19">cezar.murariu</option>
                              <option value="83">ciprian.albu</option>
                              <option value="109">corina.bogos</option>
                              <option value="38">cristian.dima</option>
                              <option value="14">cristian.petrescu</option>
                              <option value="105">daniel.canila</option>
                              <option value="106">daniel.liche</option>
                              <option value="86">daniel.motfolea</option>
                              <option value="22">dragos.dascalescu</option>
                              <option value="55">dragos.honciuc</option>
                              <option value="107">dragos.vieru</option>
                              <option value="104">emil.gugulica</option>
                              <option value="16">florin.serban</option>
                              <option value="103">gabriela</option>
                              <option value="27">george.sumanaru</option>
                              <option value="7">iulian.gaftoneanu</option>
                              <option value="67">juganariu.madalin</option>
                              <option value="11">marius.mahu</option>
                              <option value="15">mihai.hergheligiu</option>
                              <option value="20">ovidiu.romanescu</option>
                              <option value="5">paul.rotaru</option>
                              <option value="46">petrica.munteanu</option>
                              <option value="8">radu.vraciu</option>
                              <option value="59">razvan.ujica</option>
                              <option value="95">alin.patru</option>
                              <option value="87">samili.sihamadov</option>
                              <option value="25">sami.motfolea</option>
                              <option value="21">sebastian.florea</option>
                              <option value="13">sebastian.motfolea</option>
                              <option value="1">sergiu</option>
                              <option value="6">sergiuop</option>
                              <option value="66">stefan.petrescu</option>
                              <option value="4">testoperator</option>
                              <option value="10">travis.aeroport</option>
                              <option value="12">travis.bacau</option>
                              <option value="96">travis.brasov</option>
                              <option value="99">travis.cluj</option>
                              <option value="28">travis.suceava</option>
                              <option value="100">travis.timisoara</option>
                              <option value="65">veorel.mahu</option>
                              <option value="84">virgil.carciumaru</option>
                              <option value="54">balan.vlad</option>
                            </select></td>
                          <td><input type="text" name="alte_cheltuieli_suma2" id="alte_cheltuieli_suma2" value="0"
                              class="form-control input_decont" style="width: 50px;" placeholder="suma" /></td>

                          <td><input type="text" name="alte_cheltuieli_detalii2" id="alte_cheltuieli_detalii2" value=""
                              class="form-control select_decont" placeholder="info" /></td>
                          <td></td>
                        </tr>


                        <tr>
                          <td colspan="8">&nbsp;</td>
                        </tr>

                        <tr>

                          <td class="coloana_total">Total incasari </td>
                          <td style="font-weight:bold; text-transform: uppercase; font-size: 20px; padding-left: 10px;">
                            <span id="total_incasari">140</span>

                          </td>
                          <td style="font-weight:bold; text-transform: uppercase; font-size: 20px;"><span
                              id="tarif_total_preview"></span></td>
                          <td class="coloana_total">Total cheltuieli</td>
                          <td></td>
                          <td style="font-size: 20px; font-weight:bold; text-transform: uppercase;"><span
                              id="total_cheltuieli">0</span></td>
                          <td></td>
                          <td></td>
                        </tr>

                        <tr>
                          <td colspan="8">&nbsp;</td>
                        </tr>

                        <tr>
                          <td colspan="8">
                            <table>
                              <tr>
                                <td>
                                  Factura 1
                                </td>
                                <td>
                                  <select name="agent_factura_1" id="agent_factura_1"
                                    class="form-control select_decont">
                                    <option value="0">-</option>
                                    <option value="2">adrian</option>
                                    <option value="98">alexgalben</option>
                                    <option value="97">alexandru.galan</option>
                                    <option value="26">andrei.ciuta</option>
                                    <option value="108">andrei.radu</option>
                                    <option value="101">andrei.sofron</option>
                                    <option value="17">andrei.zamosteanu</option>
                                    <option value="19">cezar.murariu</option>
                                    <option value="83">ciprian.albu</option>
                                    <option value="109">corina.bogos</option>
                                    <option value="38">cristian.dima</option>
                                    <option value="14">cristian.petrescu</option>
                                    <option value="105">daniel.canila</option>
                                    <option value="106">daniel.liche</option>
                                    <option value="86">daniel.motfolea</option>
                                    <option value="22">dragos.dascalescu</option>
                                    <option value="55">dragos.honciuc</option>
                                    <option value="107">dragos.vieru</option>
                                    <option value="104">emil.gugulica</option>
                                    <option value="16">florin.serban</option>
                                    <option value="103">gabriela</option>
                                    <option value="27">george.sumanaru</option>
                                    <option value="7">iulian.gaftoneanu</option>
                                    <option value="67">juganariu.madalin</option>
                                    <option value="11">marius.mahu</option>
                                    <option value="15">mihai.hergheligiu</option>
                                    <option value="20">ovidiu.romanescu</option>
                                    <option value="5">paul.rotaru</option>
                                    <option value="46">petrica.munteanu</option>
                                    <option value="8">radu.vraciu</option>
                                    <option value="59">razvan.ujica</option>
                                    <option value="95">alin.patru</option>
                                    <option value="87">samili.sihamadov</option>
                                    <option value="25">sami.motfolea</option>
                                    <option value="21">sebastian.florea</option>
                                    <option value="13">sebastian.motfolea</option>
                                    <option value="1">sergiu</option>
                                    <option value="6">sergiuop</option>
                                    <option value="66">stefan.petrescu</option>
                                    <option value="4">testoperator</option>
                                    <option value="10">travis.aeroport</option>
                                    <option value="12">travis.bacau</option>
                                    <option value="96">travis.brasov</option>
                                    <option value="99">travis.cluj</option>
                                    <option value="28">travis.suceava</option>
                                    <option value="100">travis.timisoara</option>
                                    <option value="65">veorel.mahu</option>
                                    <option value="84">virgil.carciumaru</option>
                                    <option value="54">balan.vlad</option>
                                  </select>
                                </td>
                                <td>
                                  <input type="text" name="nr_factura_1" id="nr_factura_1" value=""
                                    class="form-control " placeholder="Numar factura 1" />
                                </td>
                                <td>
                                  <input type="text" name="suma_factura_1" id="suma_factura_1" value=""
                                    class="form-control " placeholder="Suma factura 1" />
                                </td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                              </tr>
                            </table>
                          </td>

                        </tr>

                        <tr>
                          <td colspan="8">
                            <table>
                              <tr>
                                <td>
                                  Factura 2
                                </td>
                                <td>
                                  <select name="agent_factura_2" id="agent_factura_2"
                                    class="form-control select_decont">
                                    <option value="0">-</option>
                                    <option value="2">adrian</option>
                                    <option value="98">alexgalben</option>
                                    <option value="97">alexandru.galan</option>
                                    <option value="26">andrei.ciuta</option>
                                    <option value="108">andrei.radu</option>
                                    <option value="101">andrei.sofron</option>
                                    <option value="17">andrei.zamosteanu</option>
                                    <option value="19">cezar.murariu</option>
                                    <option value="83">ciprian.albu</option>
                                    <option value="109">corina.bogos</option>
                                    <option value="38">cristian.dima</option>
                                    <option value="14">cristian.petrescu</option>
                                    <option value="105">daniel.canila</option>
                                    <option value="106">daniel.liche</option>
                                    <option value="86">daniel.motfolea</option>
                                    <option value="22">dragos.dascalescu</option>
                                    <option value="55">dragos.honciuc</option>
                                    <option value="107">dragos.vieru</option>
                                    <option value="104">emil.gugulica</option>
                                    <option value="16">florin.serban</option>
                                    <option value="103">gabriela</option>
                                    <option value="27">george.sumanaru</option>
                                    <option value="7">iulian.gaftoneanu</option>
                                    <option value="67">juganariu.madalin</option>
                                    <option value="11">marius.mahu</option>
                                    <option value="15">mihai.hergheligiu</option>
                                    <option value="20">ovidiu.romanescu</option>
                                    <option value="5">paul.rotaru</option>
                                    <option value="46">petrica.munteanu</option>
                                    <option value="8">radu.vraciu</option>
                                    <option value="59">razvan.ujica</option>
                                    <option value="95">alin.patru</option>
                                    <option value="87">samili.sihamadov</option>
                                    <option value="25">sami.motfolea</option>
                                    <option value="21">sebastian.florea</option>
                                    <option value="13">sebastian.motfolea</option>
                                    <option value="1">sergiu</option>
                                    <option value="6">sergiuop</option>
                                    <option value="66">stefan.petrescu</option>
                                    <option value="4">testoperator</option>
                                    <option value="10">travis.aeroport</option>
                                    <option value="12">travis.bacau</option>
                                    <option value="96">travis.brasov</option>
                                    <option value="99">travis.cluj</option>
                                    <option value="28">travis.suceava</option>
                                    <option value="100">travis.timisoara</option>
                                    <option value="65">veorel.mahu</option>
                                    <option value="84">virgil.carciumaru</option>
                                    <option value="54">balan.vlad</option>
                                  </select>
                                </td>
                                <td>
                                  <input type="text" name="nr_factura_2" id="nr_factura_2" value=""
                                    class="form-control " placeholder="Numar factura 2" />
                                </td>
                                <td>
                                  <input type="text" name="suma_factura_2" id="suma_factura_2" value=""
                                    class="form-control " placeholder="Suma factura 2" />
                                </td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                              </tr>
                            </table>
                          </td>

                        </tr>

                        <tr>
                          <td colspan="8">
                            <table>
                              <tr>
                                <td>
                                  Factura 3
                                </td>
                                <td>
                                  <select name="agent_factura_3" id="agent_factura_3"
                                    class="form-control select_decont">
                                    <option value="0">-</option>
                                    <option value="2">adrian</option>
                                    <option value="98">alexgalben</option>
                                    <option value="97">alexandru.galan</option>
                                    <option value="26">andrei.ciuta</option>
                                    <option value="108">andrei.radu</option>
                                    <option value="101">andrei.sofron</option>
                                    <option value="17">andrei.zamosteanu</option>
                                    <option value="19">cezar.murariu</option>
                                    <option value="83">ciprian.albu</option>
                                    <option value="109">corina.bogos</option>
                                    <option value="38">cristian.dima</option>
                                    <option value="14">cristian.petrescu</option>
                                    <option value="105">daniel.canila</option>
                                    <option value="106">daniel.liche</option>
                                    <option value="86">daniel.motfolea</option>
                                    <option value="22">dragos.dascalescu</option>
                                    <option value="55">dragos.honciuc</option>
                                    <option value="107">dragos.vieru</option>
                                    <option value="104">emil.gugulica</option>
                                    <option value="16">florin.serban</option>
                                    <option value="103">gabriela</option>
                                    <option value="27">george.sumanaru</option>
                                    <option value="7">iulian.gaftoneanu</option>
                                    <option value="67">juganariu.madalin</option>
                                    <option value="11">marius.mahu</option>
                                    <option value="15">mihai.hergheligiu</option>
                                    <option value="20">ovidiu.romanescu</option>
                                    <option value="5">paul.rotaru</option>
                                    <option value="46">petrica.munteanu</option>
                                    <option value="8">radu.vraciu</option>
                                    <option value="59">razvan.ujica</option>
                                    <option value="95">alin.patru</option>
                                    <option value="87">samili.sihamadov</option>
                                    <option value="25">sami.motfolea</option>
                                    <option value="21">sebastian.florea</option>
                                    <option value="13">sebastian.motfolea</option>
                                    <option value="1">sergiu</option>
                                    <option value="6">sergiuop</option>
                                    <option value="66">stefan.petrescu</option>
                                    <option value="4">testoperator</option>
                                    <option value="10">travis.aeroport</option>
                                    <option value="12">travis.bacau</option>
                                    <option value="96">travis.brasov</option>
                                    <option value="99">travis.cluj</option>
                                    <option value="28">travis.suceava</option>
                                    <option value="100">travis.timisoara</option>
                                    <option value="65">veorel.mahu</option>
                                    <option value="84">virgil.carciumaru</option>
                                    <option value="54">balan.vlad</option>
                                  </select>
                                </td>
                                <td>
                                  <input type="text" name="nr_factura_3" id="nr_factura_3" value=""
                                    class="form-control " placeholder="Numar factura 3" />
                                </td>
                                <td>
                                  <input type="text" name="suma_factura_3" id="suma_factura_3" value=""
                                    class="form-control " placeholder="Suma factura 3" />
                                </td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                              </tr>
                            </table>
                          </td>

                        </tr>


                        <tr>
                          <td>&nbsp;</td>
                          <td></td>
                          <td></td>
                          <td></td>
                          <td></td>
                          <td></td>
                          <td></td>
                          <td></td>
                        </tr>


                        <tr id="decont-title">
                            <td colspan="3">DECONT INCHIRIERE</td>
                            <td colspan="1"><span id="total_decont">140</span> &euro;</td>
                            <td colspan="4">In asteptare</td>
                        </tr>
                      </table>

                    </div>
                  </div>

                  <div class="row" style="margin-top: 10px;">
                      <div class="col-md-6 col-sm-12">
                          <input id="salveaza-rezervare" type="submit" class="btn btn-primary" value="Salveaza Rezervarea" style="width: 100%; font-weight:bold; text-transform:uppercase;" />
                      </div>
                      <div class="col-md-6 col-sm-12">
                          <input id="salveaza-decont" type="submit" class="btn btn-primary" value="Salveaza Decont" style="width: 100%; background-color: yellow; color: #000; border-color: yellow; text-transform: uppercase; font-weight:bold;" />
                      </div>
                  </div>


                </div>
              </div>
            </div> <!-- client -->

            <div class="hk-sec-wrapper">
              <div class="panel panel-flat">
                <div class="panel-heading">
                  <h5 class="panel-title"></h5>
                  <div class="heading-elements">
                    <!--<ul class="icons-list">
                                   <li><a data-action="collapse"></a></li>
                                   <li><a data-action="reload"></a></li>
                                   <li><a data-action="close"></a></li>
                               </ul>-->
                  </div>
                </div>

                <div class="panel-body">
                  <h4 style="margin-top: -20px;">Editeaza client</h4>
                  <form name="save-client" method="post" action="?pag=rezervari&pag2=edit-rezervare&idr=43022&action=save-client">
    <div class="row">
        <div class="col-md-12">
            <h5 style="font-weight: bold; margin-top: 10px;">Date personale</h5>
            <div class="row">
                <div class="col-md-3">
                    <input type="hidden" name="client-id" value="38566" />
                    <label>Nume</label>
                    <input type="text" name="client-nume" value="test" class="form-control" />
                </div>
                <div class="col-md-3">
                    <label>Prenume</label>
                    <input type="text" name="client-prenume" value="test" class="form-control" />
                </div>
                <div class="col-md-3">
                    <label>Tara</label>
                    <input type="text" name="client-tara" value="Romania" class="form-control" />
                </div>
                <div class="col-md-3">
                    <label>Adresa</label>
                    <input type="text" name="client-adresa" value="Hh" class="form-control" />
                </div>
                <div class="col-md-3" style="padding-top: 15px;">
                    <label>Telefon</label>
                    <input type="text" name="client-telefon" value="123123" class="form-control" />
                </div>
                <div class="col-md-3" style="padding-top: 15px;">
                    <label>Email Rezervare</label>
                    <input type="text" name="client-email" value="sergiu.hriscu@gmail.com" class="form-control" />
                </div>
                <div class="col-md-3" style="padding-top: 15px;">
                    <label>Email Client</label>
                    <input type="text" name="client-email2" value="" class="form-control" />
                </div>
            </div>
            <h5 style="margin-top: 15px; font-weight: bold;">Documente</h5>
            <div class="row">
                <div class="col-md-4" style="padding-top: 15px;">
                    <label>CNP</label>
                    <input type="text" name="client-cnp" value="1900" class="form-control" />
                </div>
                <div class="col-md-4" style="padding-top: 15px;">
                    <label>Serie ID <a href="https://car.travis.ro/view_task_img.php?url=https://task.travis.ro/autoout/pd_1711721507_ci.txt" target="_blank" style="display:inline-block;">Deschide foto</a> &nbsp; <p id="butDocumenteClient1" style="cursor: pointer; font-weight: bold; display:inline-block;" title="Adauga document">Adauga foto</p></label>
                    <div id="documenteClient1" style="display: none;">
                        <label>ID / Pasaport</label>
                        <input type="file" id="predare_document_ci" class="form-control" style="width: 100%;" onchange="predare_document('ci');" />
                        <input type="file" id="predare_document_ci2" class="form-control" style="width: 100%;" onchange="predare_document('ci2');" />
                        <textarea id="predare_document_nota_ci" onchange="predare_note_document('ci');" class="form-control"></textarea>
                        <a id="saveDocumenteClient1" style="cursor:pointer; background-color: orange; color: #fff; padding: 10px;">Salveaza documente</a>
                    </div>
                    <input type="text" name="client-serie" value="Mz" class="form-control" />
                </div>
                <div class="col-md-4" style="padding-top: 15px;">
                    <label>Numar ID</label>
                    <input type="text" name="client-numar" value="34" class="form-control" />
                </div>
                <div class="col-md-12" style="padding-top: 15px;">
                    <label>Numar permis &nbsp; <p id="butDocumenteClient2" style="cursor: pointer; font-weight: bold; display:inline-block;" title="Adauga document">Adauga foto</p></label>
                    <div id="documenteClient2" style="display: none;">
                        <label>Permis conducere</label>
                        <input type="file" id="predare_document_permis" class="form-control" style="width: 100%;" onchange="predare_document('permis');" />
                        <input type="file" id="predare_document_permis2" class="form-control" style="width: 100%;" onchange="predare_document('permis2');" />
                        <textarea id="predare_document_nota_permis" onchange="predare_note_document('permis');" class="form-control"></textarea>
                        <a id="saveDocumenteClient2" style="cursor:pointer; background-color: orange; color: #fff; padding: 10px;">Salveaza documente</a>
                    </div>
                    <input type="text" name="client-permis" value="Isbn" class="form-control" />
                </div>
            </div>
            <br id="br1" />
                <br id="br2" />
                <br id="br3" />
                <br id="br4" />
                <br id="br5" />
        </div>
        <div class="col-md-12">
            <!-- mini quiz -->
            <h5 id="alte-informatii" style="font-weight:bold; color: red; margin-top: 50px; margin-bottom: 50px; ">Alte informatii</h5>
            <label id="quiz-label" for="quiz">De unde ati aflat despre noi?</label>
            <select class="form-control" name="quiz" id="quiz">
                <option value="0"></option>
                <option value="1">Cautare pe internet (Google)</option>
                <option value="2">Anunt sponsorizat pe Google</option>
                <option value="3">Retele de socializare</option>
                <option value="4">Reclama Facebook</option>
                <option value="5">Prin recomandare</option>
                <option value="6">Birou aeroport</option>
                <option value="7">Accesare directa a site-ului</option>
                <option value="8">Sunt client fidel</option>
                <option value="9">Alta sursa</option>
            </select>
            <input type="text" name="quizextra" class="form-control" value="" />
            <br /><br />
            <!-- end mini quiz -->
            <h5 style="font-weight: bold;">Informatii facturare</h5>
            <div class="row">
                <div class="col-md-3">
                    <label>Nume companie</label>
                    <input type="text" name="firma-nume" value="" class="form-control" />
                </div>
                <div class="col-md-3">
                    <label>CUI</label>
                    <input type="text" name="firma-cui" value="" class="form-control" />
                </div>
                <div class="col-md-3">
                    <label>Tara</label>
                    <input type="text" name="firma-tara" value="" class="form-control" />
                </div>
                <div class="col-md-3">
                    <label>Adresa companie</label>
                    <input type="text" name="firma-adresa" value="" class="form-control" />
                </div>
            </div>
            <div class="col-md-12">
                <input type="submit" class="btn btn-primary" name="submit-save-client" id="submit-save-client" style="width: 100%; margin-top: 100px; margin-bottom: 100px;" value="Salveaza date client" />
            </div>

        </div>
    </div>
</form>
                </div>
              </div>
            </div> <!-- checkin -->

            <!-- note si istoric -->

            <div class="hk-sec-wrapper">
              <!-- Summernote editor -->
              <div class="panel panel-flat">
                <div class="panel-heading">
                  <h5 class="panel-title"></h5>
                  <div class="heading-elements">
                    <!--<ul class="icons-list">
                                    <li><a data-action="collapse"></a></li>
                                    <li><a data-action="reload"></a></li>
                                    <li><a data-action="close"></a></li>
                                </ul>-->
                  </div>
                </div>

                <div class="panel-body" style="margin-top: 30px !important;">


                  <h4 style="margin-top: -20px;">Note rezervare #<b>43022 </b></h4>
                  <h2></h2>

                  <div class="row">
                    <div class="col-md-12">
                      <form name="adauga-nota" method="post"
                        action="?pag=rezervari&pag2=edit-rezervare&idr=43022&action=adauga-nota">
                        <textarea name="nota-rezervare" rows="5" cols="50" style="width: 100%;"></textarea>
                        <input type="submit" name="submit-add-nota" value="Adauga nota"
                          style="width: 100%; text-align: center;" />
                      </form>
                    </div>
                  </div>



                </div>
              </div>
              <!-- /summernote editor -->
            </div><!-- istoric -->


            <div class="accordion" id="accordion_1">
              <div class="card">
                <div class="card-header d-flex justify-content-between">
                  <a role="button" data-toggle="collapse" href="#collapse_1" aria-expanded="false" class="collapsed"
                    style="color:#000 !important;">Istoric rezervare</a>
                </div>
                <div id="collapse_1" class="collapse" data-parent="#accordion_1" role="tabpanel" style="">
                  <div class="card-body pa-15">
                    <div class="row" style="margin-top: 20px; padding: 15px; border: 1px solid #ccc;">
                      <div class="col-md-12">
                        <b>29.03.2024 16:09</b> <br />
                        <br /><br />
                        Tip tarif: <b>Standard</b> <br />Hyundai i10 [2023] [Travis Iasi (online)] [NORD TOUR] [B 117
                        BES] sau sau similar | - Mini<br />- inchiriere: 4 zi(le) x 35 EUR/zi = 140<br />- preluare Iasi
                        (21/10/2024 | 12:00) = 0<br />- predare Iasi (25/10/2024 | 12:00) = 0<br />- tarif extraoptiuni
                        = 0<br />- total = 140<br /> Garantie: 300<br /> Km inclusi: 1600 <br /> Nr.zbor: <br /> <br />
                        Extraoptiuni: <br />&nbsp; &nbsp; <select onchange="changeIstoricVisibility(38466)">
                          <option value="0">Privat</option>
                          <option value="1">Public</option>
                        </select>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

            </div> <!-- panel infor sursa rezervare -->

            <div class="accordion" id="accordion_2">
              <div class="card">
                <div class="card-header d-flex justify-content-between">
                  <a role="button" data-toggle="collapse" href="#collapse_2" aria-expanded="false" class="collapsed"
                    style="color:#000 !important;">Detalii rezervare</a>
                </div>
                <div id="collapse_2" class="collapse" data-parent="#accordion_2" role="tabpanel">
                  <div class="card-body pa-15">

                    Rezervare efectuata prin intermediul: rentacar.travis.ro&nbsp; &nbsp; Dispozitiv: MacOS </div>
                </div>
              </div>


            </div> <!-- panel istoric documente -->



            <div class="accordion" id="accordion_3">
              <div class="card">
                <div class="card-header d-flex justify-content-between">
                  <a role="button" data-toggle="collapse" href="#collapse_3" aria-expanded="false" class="collapsed"
                    style="color:#000 !important;">Istoric documente</a>
                </div>
                <div id="collapse_3" class="collapse" data-parent="#accordion_3" role="tabpanel">
                  <div class="card-body pa-15">

                    <table style="width: 100%;">
                      <thead>
                        <td>Data</td>
                        <td>Operator</td>
                        <td>Document</td>
                        <td>Optiuni</td>
                      </thead>
                      <tbody>
                        <tr>
                          <td>29.03.2024 16:16</td>
                          <td>sergiu hriscu</td>
                          <td>Contract + Anexa TASK - 1.1. Contract Travis (Pers. Fizica) [TASK]</td>
                          <td><a href="https://car.travis.ro/seclog.php?idl=15145" target="_blank">Vezi document</a>
                          </td>
                        </tr>
                      </tbody>
                    </table>

                  </div>
                </div>
              </div>


            </div>
            <!-- decont -->


            <div class="accordion" id="accordion_11">
              <div class="card">
                <div class="card-header d-flex justify-content-between">
                  <a role="button" data-toggle="collapse" href="#collapse_11" aria-expanded="false" class="collapsed"
                    style="color:#000 !important;">Istoric decont</a>
                </div>
                <div id="collapse_11" class="collapse" data-parent="#accordion_11" role="tabpanel" style="">
                  <div class="card-body pa-15">
                  </div>
                </div>
              </div>

            </div>


          </div>

          <div class="modal fade" id="modalLinkUnic" tabindex="-1" aria-labelledby="myModalLabel" aria-hidden="true">
            <div class="modal-dialog">
              <div class="modal-content">

                <div class="modal-header">
                  <button type="button" class="close" data-dismiss="modal">&times;</button>
                  <h5 class="modal-title">Genereaza link unic task</h5>
                </div>
                <div class="modal-body">
                  <div class="mb-3">
                    <div id="output-link" style="font-size: 20px; text-align:center;"></div>
                  </div>
                  <div class="mb-3">
                    <label>Cui doresti sa trimiti?</label>
                    <select id="utilizator-link" class="form-control">
                      <option value="0">- selecteaza -</option>
                      <option value="2">Adrian Gradinaru</option>
                      <option value="98">Alex Galben</option>
                      <option value="97">Alexandru Galan</option>
                      <option value="26">Andrei Ciuta</option>
                      <option value="108">Andrei Radu</option>
                      <option value="101">Andrei Sofron</option>
                      <option value="17">Andrei Zamosteanu</option>
                      <option value="19">Cezar Murariu</option>
                      <option value="83">Ciprian Albu</option>
                      <option value="109">Corina Bogos</option>
                      <option value="38">Cristian Dima</option>
                      <option value="14">Cristian Petrescu</option>
                      <option value="105">Daniel Canila</option>
                      <option value="106">Daniel Liche (Bucuresti)</option>
                      <option value="86">Daniel Motfolea</option>
                      <option value="22">Dragos Dascalescu</option>
                      <option value="55">Dragos Honciuc</option>
                      <option value="107">Dragos Vieru</option>
                      <option value="104">Emil Gugulica</option>
                      <option value="16">Florin Serban</option>
                      <option value="103">gabriela ciurlica</option>
                      <option value="27">George Sumanaru</option>
                      <option value="7">Iulian Gafto</option>
                      <option value="67">Juganariu Madalin</option>
                      <option value="11">Marius Mahu</option>
                      <option value="15">Mihai Hergheligiu</option>
                      <option value="20">Ovidiu Romanescu</option>
                      <option value="5">Paul Rotaru</option>
                      <option value="46">Petrica Munteanu</option>
                      <option value="8">Radu Vraciu</option>
                      <option value="59">Razvan Ujica</option>
                      <option value="95">safetravel</option>
                      <option value="87">Samili Sihamadov</option>
                      <option value="25">Samuel Motfolea</option>
                      <option value="21">Sebastian Florea</option>
                      <option value="13">Sebastian Motfolea</option>
                      <option value="1">sergiu hriscu</option>
                      <option value="6">sergiuop</option>
                      <option value="66">Stefan Petrescu (Bucuresti)</option>
                      <option value="4">test operator</option>
                      <option value="10">Travis Aeroport Iasi</option>
                      <option value="12">Travis Bacau</option>
                      <option value="96">Travis Brasov</option>
                      <option value="99">Travis Cluj</option>
                      <option value="28">Travis Suceava</option>
                      <option value="100">Travis Timisoara</option>
                      <option value="65">Veorel Mahu</option>
                      <option value="84">Virgil Carciumaru</option>
                      <option value="54">Vlad Balan</option>
                    </select>
                  </div>

                  <div class="mb-3">

                    <label>Ce flow?</label>
                    <select id="flow-link" class="form-control">
                      <option value="0">- selecteaza -</option>
                      <option value="predare">Predare auto</option>
                      <option value="preluare">Preluare auto</option>

                    </select>
                  </div>

                  <div class="mb-3">
                    <label>Valabilitate link</label>
                    <table style="width: 100%;">
                      <tr>
                        <td>De la</td>
                        <td><input type="date" class="form-control" id="data1-link" value="2024-04-08" /></td>
                        <td><input type="time" class="form-control" id="ora1-link" value="10:45" /></td>
                      </tr>
                      <tr>
                        <td>Pana la</td>
                        <td><input type="date" class="form-control" id="data2-link" value="2024-04-09" /></td>
                        <td><input type="time" class="form-control" id="ora2-link" value="10:45" /></td>
                      </tr>
                    </table>

                  </div>



                  <button onclick="generareLinkTask();" type="submit" class="btn btn-primary">Genereaza</button>

                </div>
              </div>
            </div>
          </div>

          <div id="notification"
            style="display: none; background-color:#000; color:#fff; z-index:99999; padding: 15px; border-radius: 10px; position:fixed; width: 95%; left:2%; bottom:20px; font-size: 14px;">
          </div>

          <iframe
            src="https://rentacar.travis.ro/admin/?log-operator-remote=abc123zzyySSAA2231&adminLogare=daDA&user=Q3Z0ejVUK2VxTCtZcWRiQUpXRFBHUT09&id=d2dEYmM0eHpNNEV6aDZkNzFoWHVXUT09&numeComplet=KzVwSG83UTlNeWRhNTAxVE84UENhdz09&email=SGZHK09tZmJoSEs0S3U3bU1FWEJSME1lK2tJZE5vdURRYWpSQ3JxOW9NWT0=&rol=administrator&rezervari=1&locatii=0&flota=1&furnizori=0&site=0&emailuri=0&utilizatori=0&rapoarte=0"
            width="1" height="1"></iframe><iframe
            src="https://romaniarentacar.eu/admin/?log-operator-remote=abc123zzyySSAA2231&adminLogare=daDA&user=Q3Z0ejVUK2VxTCtZcWRiQUpXRFBHUT09&id=d2dEYmM0eHpNNEV6aDZkNzFoWHVXUT09&numeComplet=KzVwSG83UTlNeWRhNTAxVE84UENhdz09&email=SGZHK09tZmJoSEs0S3U3bU1FWEJSME1lK2tJZE5vdURRYWpSQ3JxOW9NWT0=&rol=administrator&rezervari=1&locatii=0&flota=1&furnizori=0&site=0&emailuri=0&utilizatori=0&rapoarte=0"
            width="1" height="1">
          </iframe>
  </div>
</div>
  <!-- /HK Wrapper -->


    </body>

    </html>
  </div>

  <div id="notification"
    style="display: none; background-color:#000; color:#fff; z-index:99999; padding: 15px; border-radius: 10px; position:fixed; width: 95%; left:2%; bottom:20px; font-size: 14px;">
  </div>

  <iframe
    src="https://rentacar.travis.ro/admin/?log-operator-remote=abc123zzyySSAA2231&adminLogare=daDA&user=Q3Z0ejVUK2VxTCtZcWRiQUpXRFBHUT09&id=d2dEYmM0eHpNNEV6aDZkNzFoWHVXUT09&numeComplet=KzVwSG83UTlNeWRhNTAxVE84UENhdz09&email=SGZHK09tZmJoSEs0S3U3bU1FWEJSME1lK2tJZE5vdURRYWpSQ3JxOW9NWT0=&rol=administrator&rezervari=1&locatii=0&flota=1&furnizori=0&site=0&emailuri=0&utilizatori=0&rapoarte=0"
    width="1" height="1"></iframe><iframe
    src="https://romaniarentacar.eu/admin/?log-operator-remote=abc123zzyySSAA2231&adminLogare=daDA&user=Q3Z0ejVUK2VxTCtZcWRiQUpXRFBHUT09&id=d2dEYmM0eHpNNEV6aDZkNzFoWHVXUT09&numeComplet=KzVwSG83UTlNeWRhNTAxVE84UENhdz09&email=SGZHK09tZmJoSEs0S3U3bU1FWEJSME1lK2tJZE5vdURRYWpSQ3JxOW9NWT0=&rol=administrator&rezervari=1&locatii=0&flota=1&furnizori=0&site=0&emailuri=0&utilizatori=0&rapoarte=0"
    width="1" height="1">
  </iframe>

  <!-- /HK Wrapper -->


</template>
