Sistema Servidor de Factura Electronica AFIP (01/02/2011)</br>
Copyright (C) 2011 by Baseware Systems</br>

1.0.0 - 08/02/2011 - Version inicial.</br>
      - 02/03/2011 - Renombrado como SFE. Version Beta.</br>
      - 24/03/2011 - Version candidata (RC).</br>
      - 01/04/2011 - Version RTM en el cliente.</br>
1.0.1 - 07/04/2011 - Verifica que solo pueda ejecutarse una instancia por sesion o sistema.</br>
                   - Temporizador para reutilizar el TA por un tiempo predeterminado.</br>
                   - Enviar correo a mas de una casilla de destino, CC y BCC.</br>
                   - La falta de impresoras no cierra el sistema. Solo avisa.</br>
1.0.2 - 08/04/2011 - Cambio de mensajes de error de eventos por formulario (MsgBox por FrmMsgBox).</br>
                   - Delay de lectura de archivos de 1000 a 500 mseg.</br>
                   - No se requiere activacion para modo de prueba. Solo para uso en produccion.</br>
                   - Retry para generacion del codigo de barras en Invoice.</br>
                   - Se agrego componente para asignar impresora predeterminada.</br>
      - 10/04/2011 - Agregado del numero de build para identificar versiones (Desde el 15738).</br>
                   - Se modifico funcion DigitoCAI por error al obtener el valor. Se elimino delay.</br>
      - 11/04/2011 - Se cambio el tiempo de retry de lectura del archivo de registro a 1000 mseg.</br>
      - 17/04/2011 - Se cambio el color del texto segun el estado de la emision.</br>
      - 27/04/2011 - Se corrigio el mensaje de error que brinda la clase clsCDOmail.</br>
                   - Se actualizo la forma de generar el numero de Build.</br>
                   - Se cambio color verde basico (vbGreen) por RGB(32,160,32).</br>
1.1.0 - 10/05/2011 - Se comienza a implementar componente WSFEv1.</br>
      - 26/06/2011 - Version candidata (RC).</br>
      - 01/07/2011 - Version RTM en el cliente.</br>
      - 02/08/2011 - Se corrigio la forma de comparar y obtener WSAAKillTime.</br>
1.1.1 - 03/07/2012 - Se corrigio un problema de sincronismo entre el CloseHandle y el DeleteFile.</br>
                   - Se actualizo el formulario FrmAbout.</br>
      - 07/07/2012 - Se agrego un retardo (1000 mseg) en la funcion SetDefaultPrinter.</br>
      - 14/09/2012 - Se modifico el valor por defecto de la variable PrintCopyTxt a True.</br>
      - 19/02/2014 - Se modifico el titulo de los frames del formulario FrmProp.</br>
1.1.2 - 02/03/2014 - Se invirtieron los nombres de los TextBox TbxIn y TbxOut.</br>
                   - Se invirtieron los nombres de las variables PathCmpSend y PathCmpRecv.</br>
      - 06/03/2014 - Se protegio el chequeo de activacion del SFE de la activacion del formulario.</br>
      - 25/03/2014 - Se agrego la variable WSAACUIT para controlar con que CUIT se obtuvo el ticket.</br>
      - 04/04/2014 - Se agrego el switch -CLEAR para borrar los archivos de las carpetas In/Out.</br>
      - 02/07/2014 - Se corrigio la funcion MailDir de la clase clsCDOmail para eliminar ";" sobrantes.</br>
1.1.3 - 02/08/2014 - Se efectuaron modificaciones para permitir funcionamiento multi CUIT y WebService.</br>
                   - Se agrego el Codigo de RG para obtener comprobante emitido y codificadores.</br>
      - 08/08/2014 - Se efectuaron modificaciones que posibilitan obtener CAEA e informar comprobantes.</br>
      - 12/08/2014 - Se agrego CUIT en el string de respuesta de obtencion y/o consulta de CAEA.</br>
      - 19/08/2014 - Se efectuaron correcciones esteticas. Prueba de implementacion de CAEA OK.</br>
      - 19/03/2015 - Se implemento Codigos Opcionales para Factura 'A'. Debe utilizarse con WSFEv1 Ver 1.15b.</br>
                   - Se agrego la informacion de versiones de WSAA, WSFEv1 y PDFCreator en FrmAbout.</br>
      - 30/03/2015 - Se modifico la funcion Cbte para permitir generar cualquier comprobante.</br>
      - 31/03/2015 - Se modifico la funcion Cbte para imprimir el codigo de comprobante solo si es numerico.</br>
                   - Se permite generar el archivo COE a voluntad del usuario.</br>
                   - Se modifico la funcion Cbte para permitir formularios preimpresos.</br>
      - 10/04/2015 - Se agrega soporte para factura de exportacion.</br>
      - 13/04/2015 - Se homologa para WSAA Ver 2.08a, WSFEv1 Ver 1.16b, WSFEXv1 Ver 1.08c.</br>
      - 14/04/2015 - Se actualizo FrmAbout para informar version del WSFEXv1.</br>
      - 16/04/2015 - Correcciones menores.</br>
      - 18/04/2015 - Se cambio la ubicacion de los campos CAE/CAEA, GenCOE y Preimpreso.</br>
                   - Se desdoblo el campo Filler para crear el numero de copias, CAE/CAEA, GenCOE y Preimpreso.</br>
      - 01/05/2015 - Se desdoblo el campo Filler para crear Imprimir Pie de Pagina L/R solo en la ultima hoja.</br>
      - 13/05/2015 - Se corrigio un error de desbordamiento en la funcion ConvNum.</br>
      - 30/05/2015 - Se agregaron los CheckBox en el FrmProp para informar los switches -START y -CLEAR.</br>
      - 01/06/2015 - Se modifico la posicion del Sleep(1000) en la funcion SetDefaultPrinter.</br>
      -            - Se agrego la definicion de la impresora predeterminada en la funcion SetDefaultPrinter.</br>
      - 02/06/2015 - Se elimino el delay Sleep(1000) de la funcion SetDefaultPrinter por superfluo.</br>
      - 03/06/2015 - Se agrego un espacio delante del titulo de la ventana en la sub ShowMsg por estetica.</br>
      - 16/06/2015 - Se corrigio ByVal por ByRef en la funcion GetWSAA porque no devolvia errores.</br>
      - 01/10/2015 - Se centra el logo en el rectangulo disponible.</br>
1.1.4 - 14/05/2016 - Se agrego chequeo de vencimiento de certificados y aviso por mail.</br>
      - 12/06/2016 - Se agrego bloqueo de cierre de sesion o apagado del sistema.</br>
      - 07/09/2016 - Se agrego el componente REGTOOL5.DLL (BWActivate.dll) que faltaba en el paquete de instalacion.</br>
      - 08/09/2016 - Se corrigio ubicacion de instalacion del archivo certmgr.exe.</br>
      - 01/02/2017 - Se permite informar un archivo como fuente de direcciones de correo o las direcciones de correo.</br>
      - 02/01/2018 - Se efectuo una modificacion a SetDefaultPrinter para no mostrar error si la impresora por defecto es PDFPrinter.</br>
      - 29/09/2018 - Se permite informar un archivo como fuente del texto del mensaje o el mensaje.</br>
      - 06/02/2019 - Se rectifico la generacion del PDF con punto de venta a 5 digitos.</br>
1.1.5 - 23/08/2019 - Se actualizo la aplicacion para adecuarla a las modificaciones en Tipo de Comprobante y Punto de Venta.</br>
      - 31/08/2019 - Se adecua la aplicacion para Factura de Credito Electronica (FCE).</br>
      - 04/09/2019 - Se homologa para WSAA Ver 2.11c, WSFEv1 Ver 1.23b, WSFEXv1 Ver 1.08c.</br>
                   - Se agrando el campo Archivo a 3000 y se quitaron espacios en CUIT alternativo de WSFEXv1 para mostrar en grilla.</br>
      - 02/10/2019 - Se corrigio un error en la presentacion del numero de comprobante en el log.</br>
      - 09/06/2020 - Se corrigio un error en la descripcion al abrir el selector de carpetas en SrvToAFIP y AFIPToSrv.</br>
      - 16/06/2020 - Se actualizo el control BarcodeWiz de la version 2.0 a 7.1.</br>
1.2.0 - 10/09/2020 - Se actualizo el PDFCreator para utilizar las versiones posteriores a la 2.0.</br>
      - 14/09/2020 - Se elimino la referencia al PDFCreator en el IDE del VB6 porque no es necesaria.</br>
      - 17/09/2020 - Se utiliza el PDFCreator para crear el PDF y el PDFtoPrinter para imprimirlo.</br>
      - 28/09/2020 - Se corrigio un problema con la obtencion del path a la carpeta Program Files en FrmAbout.</br>
                   - Se corrigio la funcion GetSystemDir porque no devolvia un string correcto en 64 bits.</br>
      - 05/10/2020 - Se efectuaron cambios en el texto de algunos mensajes de error.</br>
                   - Si se detecta que algun certificado esta por vencer, solo se envia correo si fue informada alguna direccion.</br>
      - 08/11/2020 - Se corrigieron los codigos de comprobantes para FAM, NDM, NCM y REM en el archivo comprobantes.txt.</br>
      - 20/11/2020 - Se mejoraron redundancias de codigo reemplazandolos por subrutinas en FrmProp.</br>
1.2.1 - 27/12/2020 - Cambio de CB a QR por RG AFIP. Se elimina el componente BarCodeWiz y se agregan el FreeImage.dll y QRCode.exe.</br>
      - 11/01/2021 - Se agrego en Invoice los comprobantes letra 'M' omitidos por error.</br>
      - 29/01/2021 - Correccion menor en la funcion QRCode. Se cambio de posicion la variable QRCode.</br>
      - 04/02/2021 - Se corrigio un error en el FrmProp que se producia al cambiar el nombre del archivo de Log y si este no existia.</br>
      - 06/02/2021 - Se cambio el modulo BMPConvert por el MFreeImage. Se carga directamente el PNG a traves de la funcion LoadPictureEx. Se requiere FreeImage.dll.</br>
      - 16/02/2021 - Se utiliza BWActivate Ver 1.0.2. Soluciona problemas de activacion en servidores virtuales de 32 o 64 bits.</br>
      - 06/03/2021 - Si no se ha activado el SFE se reemplazan linea de detalle de impresion cada 5 lineas y del CAE solo se muestran los primeros 10 digitos.</br>
      - 09/03/2021 - Se agrego verificacion de lectura del PDF luego de su creacion para evitar errores de sincronismo.</br>
      - 23/03/2021 - Se cambio la posicion del identificador de copia, ahora se coloca debajo de la fecha de vencimiento del CAE.</br>
      - 25/03/2021 - Se corrigio la carpeta utilizada para verificar los CRT en la solapa Certficados. Ahora se utiliza la informada en TbxCrt.</br>
1.2.2 - 01/04/2021 - Se utiliza el PDFCreator para impresion y se descarta el PDFtoPrinter por presentar problemas con ventanas emergentes.</br>
                   - Nuevo icono para festejar los 10 años del producto.</br>
      - 02/04/2021 - Agregado de detalles para ver las propiedades del PDF con cualquier visor.</br>
      - 05/04/2021 - Se debio colocar el viejo icono porque el nuevo informaba error, aparentemente en sistemas de 64 bits.</br>
      - 07/04/2021 - Se convirtieron a string los valores en los paneles del StatusBar y sus ToolTipText.</br>
      - 08/04/2021 - Se agrego "On Error Resume Next" en la funcion WSAACertInfo en el caso de no haber instalado previamente el componente WSAA.</br>
      - 16/04/2021 - Se agrego el registro 4 para que el usuario pause la ejecucion hasta un maximo de 60 segundos.</br>
      - 25/05/2021 - Se agrego la posibilidad de pausar la ejecucion luego de la generacion del PDF.</br>
-------------------------------------------------------------------------------------------------------------------------------------------------------------
