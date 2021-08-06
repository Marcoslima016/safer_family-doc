
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<style>

.myButton {
	background-color:#44c767;
	border-radius:9px;
	border:1px solid #18ab29;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:17px;
	padding:16px 31px;
	text-decoration:none;
	text-shadow:0px 1px 0px #2f6627;
}
.myButton:hover {
	background-color:#5cbf2a;
}
.myButton:active {
	position:relative;
	top:1px;
}


</style>

## Lista de Devices
---

| Referência | ID |   | 
|:-----------:|:-----------:|-----------:|  
| 3 | FFFFFFF | [Gerar QR :fontawesome-solid-qrcode:](#){ .md-button .md-button--primary } |
| 4 | FFFFFFF | [Gerar QR :fontawesome-solid-qrcode:](#){ .md-button .md-button--primary } |
| 5 | FFFFFFF | [Gerar QR :fontawesome-solid-qrcode:](#){ .md-button .md-button--primary } |

## Parâmetros e Funcionamento
---

Nesse tópico será abordado a rotina de funcionamento dos devices Safer, e as tecnologias envolvidas. 


### 1. Tecnologias utilizadas

O device utiliza duas tecnologias de comunicação: 

* Beacon
* BLE

</br>

** 1. Beacon: **  Tecnologia que trabalha baseada em regiões.

** 2. BLE: **  Tecnologia tradicional do bluetooth.


</br></br>
### 2. Funcionamento geral


</br></br>
### 3. Rotinas

** A. Rotina quando não há smartphone conectado ao device via BLE: ** 

Enquanto não houver smartphone conectado ao device via BLE, as duas regiões do beacon são transmitidas, dessa forma é possível identificar se ja tem algum smartphone conectado ao device (isso será útil no app mobile).


<img src="../assets/rotina1.png" alt="drawing" width="100%"/>

</br>

** B. Rotina quando houver smartphone conectado ao device : ** 

Quando um smartphone conecta-se ao device via BLE, a rotina muda e passa a transmitir apenas o UUID 1. 

<img src="../assets/rotina1.png" alt="drawing" width="100%"/>


</br></br>
### 3. Resumo Parametros


<table>
  <!-------------- HEADER -------------->
  <tr bgcolor="grey" style="color:white; text-align:center">
     <td></td>
    <td  style="text-align:center; vertical-align:middle;"><b>Sem conexão BLE</b></td>
    <td style="text-align:center; vertical-align:middle;"><b>Conectado ao BLE</b></td>

  </tr>
    <!-------------- DATA -------------->
  <tr style="text-align:center">
    <td style="text-align:center"> <b> Inicialização </b> </td>
    <td style="text-align:center"> 30s </td>
    <td style="text-align:center"> 30s </td>
  </tr>	
  <tr style="text-align:center">
    <td style="text-align:center"> <b> UUID 1 </b> </td>
    <td style="text-align:center"> 30s </td>
    <td style="text-align:center"> 30s </td>
  </tr>
  <tr style="text-align:center">
    <td style="text-align:center"> <b> UUID 2 </b> </td>
    <td style="text-align:center"> 30s </td>
    <td style="text-align:center"> - </td>
  </tr>  
  <tr style="text-align:center">
    <td style="text-align:center"> <b> Anúncio BLE </b> </td>
    <td style="text-align:center"> 30s </td>
    <td style="text-align:center"> 30s </td>
  </tr>  

</table>


