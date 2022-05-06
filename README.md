# Dataset
Para atrapar todos los casos en los que el bot no funcionó se generaran nuevas columnas con la siguiente información. Además queremos observar los casos en los que se trató de una persona que no estaba registrada en el sistema.


- [x] Perdón, no te puedo ayudar con eso. Solamente ayudo con temas relacionados con nuestro centro de salud. (**No_Correlation)** No incluída en achieve
- [x] No se encuentra registrado ese DNI en el sistema. Para darte de alta por favor completá el siguiente formulario: https://forms.gle/YeRNkXYVuMh9wX2S7 y a las 24hs ya podrás operar por el sistema de turnos. **(not_DNI)** incluímos o no en achieves=?

- [x] Error interno. **(Error_Interno)** No incluída en achieve
- [x] Por el momento el sistema de gestión de turnos no está disponible, intente más tarde. 
👉🏻 Para comunicarte con un representante humano, escribe hablar con humano. 
Si es una urgencia, por favor comunicate al teléfono o acudí de forma presencial al centro de salud. 
Disculpe las molestias ocasionadas. **(Error_501)**
- [x] “En este momento el especialista cubrió el cupo de consultas diarias con la obra social seleccionada, te aconsejamos que busques otros días disponibles:” **(Has_Cupo)** Incluída en achieve
- [x] Se atrapa cuando el bot menciona quien es kunan. Esto sirve para ver como funcionan los intent del bot. 'Ask_Kunan'
- [x] Se atrapa error de falla api externo - **utter_falla_api_externo** . 'Falla_Api_Externo'
- [x] Se atrapan errores --> problemas de entendimiento **utter_many_fallbacks_goto_hh** . 'Many_Fallbacks_Goto_HH'

Se agregaron nuevas funciones para reconocer los/as dres/as que presentaron mayor cantidad de veces no cupo (doctor_sin_cupo) y las especialidades (msp_sin_cupo). Considerar los valores mayores a 10
