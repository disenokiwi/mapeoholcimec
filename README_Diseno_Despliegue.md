# Hoja de Ruta de Relacionamiento Estratégico – CEO Holcim Ecuador
### Guía de diseño y despliegue para la web de Keyword

Este producto sigue el mismo formato que la **Hoja de Ruta del Gerente General de Banco Pichincha** (productoskeyword.com/mapeobancopichincha). La idea es publicarlo en la web de Keyword con la misma estructura, por ejemplo en la ruta `productoskeyword.com/mapeoholcim`.

Corte de información: 13 de noviembre de 2026.

---

## 1. Contenido del paquete

| Archivo / carpeta | Qué es |
|---|---|
| `index.html` | Página completa y funcional, en un solo archivo (fotos e imágenes ya incrustadas). Sirve como referencia visual exacta y también se puede publicar tal cual. |
| `README_Diseno_Despliegue.md` | Esta guía. |
| `actores.json` | Datos de los 22 actores (nombre, cargo, sector, mecanismo, textos de la ficha y nombre del archivo de foto). |
| `fotos/` | Fotos de los actores, cuadradas, en JPG. El nombre del archivo es el `id` del actor. |
| `assets/hero.jpg` | Fondo de portada (red de personas, el mismo de BP). |
| `assets/keyword-white.png` | Logo de Keyword en blanco (portada y pie). |
| `assets/holcim.png` | Logo de Holcim (caja blanca de la portada y centro del radar). |
| `assets/ico-gob.png`, `ico-gre.png`, `ico-coo.png`, `ico-lid.png` | Íconos de los cuatro sectores (los mismos de BP). |

---

## 2. Opciones de despliegue

**Opción A, la más rápida: publicar `index.html` tal cual.**
- En Wix: crear la página `mapeoholcim`, agregar **Insertar código → Insertar HTML (iframe)** a ancho completo, pegar el contenido de `index.html` y fijar una altura de unos 4.200 px en escritorio. El iframe tiene su propio scroll en celular, así que hay que revisarlo en móvil.
- En un hosting estático (Netlify, Vercel, S3, el servidor de Keyword): subir `index.html` y listo. No necesita backend.
- Lo único externo que carga es la tipografía **Figtree** de Google Fonts.

**Opción B, igual que BP: maquetarla en Wix con imágenes.**
Es como se hizo BP: cada actor es una imagen (foto + nombre + cargo) y al hacer click se abre un lightbox con la ficha también como imagen. Para esto, diseño exporta desde `index.html` o desde los textos de la sección 6:
- 14 *tiles* del radar (foto + nombre + cargo)
- 17 fichas (pop-up), que corresponden a los 14 del radar y a los 3 inmobiliarios
- 8 tarjetas de líderes empresariales

Esta opción da más control en el editor de Wix, pero toma más tiempo y cuesta más mantenerla.

**Recomendación:** usar la Opción A para publicar ya, y pasar a la B solo si se quiere editar desde Wix.

---

## 3. Estructura de la página (de arriba a abajo)

1. **Portada.** Fondo `assets/hero.jpg` con un velo azul encima. Al centro: logo Keyword en blanco, el título en mayúsculas *"HOJA DE RUTA DE RELACIONAMIENTO ESTRATÉGICO – CEO HOLCIM ECUADOR"* y debajo el logo de Holcim dentro de una caja blanca con esquinas redondeadas.
2. **Intro.** Franja azul oscuro con el texto:
   > Este producto incluye la hoja de relacionamiento para el nuevo CEO de Holcim Ecuador, estructurada por sectores, con el objetivo de facilitar su posicionamiento en el rol y ordenar un plan de acercamiento con actores prioritarios para Holcim Ecuador.
3. **Sectores.** Título *"Para la estrategia de tres meses se han considerado actores de cuatro sectores:"*, seguido de cuatro filas separadas por una línea fina. Cada fila lleva una casilla vacía del color del sector, el ícono y el texto, con el nombre del sector en negrita y color:
   - **Gobierno:** Autoridades del frente económico, productivo, energético y laboral, y tomadores de decisión con incidencia en la obra pública, la vivienda y el clima de inversión. El enfoque prioriza reuniones one-to-one para posicionamiento institucional y alineación de agenda.
   - **Gremios:** Cámaras empresariales, asociaciones sectoriales y espacios de representación del sector productivo y de la construcción. El objetivo es fortalecer el posicionamiento de Holcim en el ecosistema empresarial y articular agendas comunes.
   - **Cooperación Internacional:** Representación diplomática de Suiza y banca multilateral de desarrollo con agenda en infraestructura, vivienda y financiamiento sostenible. Se prioriza relacionamiento institucional y exploración de alianzas estratégicas.
   - **Líderes empresariales:** Referentes del sector privado con influencia económica y reputacional, y líderes del sector inmobiliario. El abordaje combina comunicaciones escritas y reuniones one-to-one.
4. **Instrucción y leyenda.** *"Para ver la ficha completa de cada actor del Radar, **hacer click en cada fotografía.**"* (la parte final en amarillo, con el ícono de la mano). Debajo va una leyenda horizontal en cuatro columnas, separadas por líneas verticales blancas:
   - Mes 01 · PRIORIDAD ALTA · barra amarilla · Gobierno
   - Mes 02 · PRIORIDAD MEDIA · barra verde · Gremios
   - Mes 03 · PRIORIDAD BAJA · barra naranja · Cooperación Internacional
   - MECANISMO DE ABORDAJE: **C** Comunicación escrita / **R** Reunión one-to-one
5. **Radar** (ver sección 5).
6. **Transversal.** Título *"TRANSVERSAL:"* y debajo una barra rosada con *"Líderes empresariales\*"*. Le sigue una grilla de **4 × 2** tarjetas. Cada tarjeta tiene la foto con aro rosado y el símbolo C o R, y debajo: **Nombre**, **Cargo** (la empresa) y **Temática clave**. No lleva la línea de mecanismo porque ya lo indica el símbolo. Al final va la nota: *"\* Líderes empresariales con mejor reputación según Ranking Merco"*. No se muestran números del ranking.
7. **Pie.** Franja negra con el logo Keyword en blanco, "©Todos los derechos reservados" y "**Contacto:** info@keyword.com.ec".

---

## 4. Estilo

**Tipografía:** Figtree (Google Fonts), con pesos 400, 600, 700 y 800.

**Colores**

| Uso | Hex |
|---|---|
| Fondo general | `#13205A` |
| Franja intro | `#0F1645` |
| Franja sectores | `#162563` |
| Radar, anillo 1 (Mes 01) | `#2F7BC1` |
| Radar, anillo 2 (Mes 02) | `#05336E` |
| Radar, anillo 3 (Mes 03) | `#0E1440` |
| Gobierno | `#F7D046` |
| Gremios | `#4DB131` |
| Cooperación Internacional | `#F2733D` |
| Líderes empresariales | `#F04FB4` |
| Resaltado (instrucción) | `#FFD500` |
| Símbolo **C** | fondo `#FFD500`, letra `#4A26A8` |
| Símbolo **R** | fondo `#4A26A8`, letra blanca, borde blanco fino |
| Pie | `#000000` |

**Foto de actor:** circular, con un aro de unos 4 px del color de su sector. El símbolo C o R es un cuadrado de esquinas apenas redondeadas, ubicado abajo a la derecha de la foto.

**Nombre:** va en una "píldora" blanca con texto azul oscuro `#0E1B33` en extra-bold. Debajo va **Cargo:** en blanco.

---

## 5. Radar

- Son círculos concéntricos con el **logo de Holcim en un círculo blanco** ubicado al centro-izquierda, igual que BP con su logo.
- Proporción del lienzo: 1300 × 1500. El centro está en (180, 750). Los radios son: círculo blanco 160, anillo 1 hasta 560, anillo 2 hasta 885, y el anillo 3 llega hasta el borde.
- Los actores se reparten en un arco a lo largo de la mitad de su anillo, con separación pareja para que no se monten:
  - **Anillo 1, Mes 01, Gobierno (6):** Luque, Cordovez, Blum, Ramírez, Gellibert, Kury
  - **Anillo 2, Mes 02, Gremios (5):** Navarro, Ponce, González, Yandun, Rosero
  - **Anillo 3, Mes 03, Cooperación (3):** Klötzli, Tristao, Mejía
- **En celular** el radar se reemplaza por tres bloques apilados (Mes 01, 02 y 03), cada uno con su color de anillo y los actores en dos columnas.
- **Pop-up de ficha** (igual a BP): tarjeta azul `#13235F` con esquinas de 40 px de radio y borde blanco fino.
  - A la izquierda: foto grande con aro del color del sector, nombre en píldora blanca y "Cargo:".
  - A la derecha, en este orden y separados por líneas del color del sector: **Perfil de impacto**, **Temática clave**, **Mecanismo de abordaje**, **Razonamiento del actor** y **Acompañamiento**. Las etiquetas van en el color del sector.
  - Tiene flechas Anterior y Siguiente para recorrer todas las fichas.

---

## 6. Actores y textos de las fichas

El texto completo de cada ficha está en `actores.json` y también se lista aquí abajo.

**Notas sobre las fotos**
- Andrew Wright no tiene foto pública. Va con silueta morada, como en BP.
- Las fotos de Luque, Navarro, González, Yandun, Tristao y Mejía están a 160 px. Si se arman imágenes grandes (Opción B), conviene conseguirlas en mayor resolución.


### Gobierno – Mes 01

#### Roberto Luque  `[R]`
- **Cargo:** Ministro de Infraestructura y Transporte
- **Perfil de impacto:** Ingeniero civil ecuatoriano, graduado como el mejor de su promoción en la Universidad Católica de Santiago de Guayaquil y con formación avanzada en ingeniería geotécnica en la Universidad de California, Berkeley. Se ha desempeñado como ministro de Transporte y Obras Públicas y como ministro encargado del sector Energía; tras la reestructuración del Ejecutivo, su cartera asumió también las competencias de Vivienda.
- **Temática clave:** Construcción
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Lidera la política de infraestructura, transporte y vivienda, sectores que concentran la mayor demanda de cemento y hormigón del país. Holcim mantiene una relación previa con el ministro, por lo que es relevante darle continuidad con el nuevo CEO en el marco de la planificación de obra pública y los programas de vivienda.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/luque.jpg`

#### Bernardo Cordovez  `[R]`
- **Cargo:** Ministro de Desarrollo Económico y Productivo
- **Perfil de impacto:** Licenciado en Administración Financiera, con trayectoria en el sector bancario y financiero. En el gobierno de Daniel Noboa fue asesor del Ministerio de Economía y Finanzas, gerente general del BIESS y presidente del Consejo Directivo del IESS. En septiembre de 2026 fue designado ministro de Desarrollo Económico y Productivo, cartera que agrupa a Economía y Finanzas, Producción, Comercio Exterior e Inversiones, y Agricultura.
- **Temática clave:** Economía
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Máxima autoridad de la política económica, fiscal y productiva del país. Sus decisiones inciden de manera directa en el clima de inversión, la política arancelaria y los incentivos a la industria nacional.
- **Acompañamiento:** Finanzas
- **Foto:** `fotos/cordovez.jpg`

#### Juan Carlos Blum  `[R]`
- **Cargo:** Ministro de Ambiente y Energía
- **Perfil de impacto:** Ingeniero mecánico por la ESPOL, con maestría en Gestión de Energía y Política Ambiental por la University of Pennsylvania; ha colaborado con el Banco Mundial y CAF. Fue asesor del Ministerio de Ambiente y Energía y gerente general de CNEL EP durante la crisis de apagones de abril de 2026. En mayo de 2026 fue designado ministro de Ambiente y Energía.
- **Temática clave:** Energía y ambiente
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Responsable de la política energética, ambiental y minera del país. Su cartera incide directamente en la continuidad del suministro eléctrico para la operación industrial y en los permisos ambientales y concesiones de Holcim.
- **Acompañamiento:** Equipo de Energía
- **Foto:** `fotos/blum.jpg`

#### Diana Ramírez Villacís  `[R]`
- **Cargo:** Ministra de Trabajo y Desarrollo Humano
- **Perfil de impacto:** Ingeniera en Gestión y Liderazgo por la Universidad Politécnica Salesiana. En el gobierno de Daniel Noboa estuvo al frente de la Secretaría Nacional de Planificación. En septiembre de 2026 fue designada ministra de Trabajo y Desarrollo Humano, cartera que integra al Ministerio de Trabajo, el Ministerio de Desarrollo Humano y la Secretaría de Pueblos y Nacionalidades.
- **Temática clave:** Laboral
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Responsable de la política laboral y de desarrollo humano del país. Su cartera regula la relación con colaboradores y contratistas, y su reciente designación permite establecer un canal directo desde el inicio de su gestión.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/ramirez.jpg`

#### Cynthia Gellibert  `[R]`
- **Cargo:** Presidenta del Consejo Directivo del IESS
- **Perfil de impacto:** Fue asesora de Daniel Noboa durante su paso por la Asamblea Nacional y, desde agosto de 2024, Secretaria General de la Administración Pública. Tras la reestructuración del Ejecutivo se desempeñó como ministra de Trabajo y, en septiembre de 2026, fue designada presidenta del Consejo Directivo del IESS. Previamente trabajó en el IESS como coordinadora provincial de Afiliación y Control Técnico de Guayas.
- **Temática clave:** Seguridad social
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Máxima autoridad del IESS y una de las funcionarias más cercanas al Presidente de la República. Holcim mantiene una relación previa con ella, por lo que es relevante darle continuidad con el nuevo CEO.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/gellibert.jpg`

#### Roberto Kury  `[R]`
- **Cargo:** Canciller de la República
- **Perfil de impacto:** Ingeniero en Ciencias de Administración con maestría en Administración de Empresas y más de 17 años de experiencia en tecnología y telecomunicaciones. Dirigió la CNT, fue director de Transformación Tecnológica y ministro de Telecomunicaciones. En junio de 2026 fue designado canciller, tras la salida de Gabriela Sommerfeld.
- **Temática clave:** Relación con Suiza
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Lidera la política exterior y la agenda de atracción de inversiones del país. Su interlocución es relevante para una empresa de origen suizo como Holcim, en términos de relación bilateral, estabilidad jurídica e inversión extranjera.
- **Acompañamiento:** NA
- **Foto:** `fotos/kury.jpg`


### Gremios – Mes 02

#### Juan Carlos Navarro Gómez  `[R]`
- **Cargo:** Presidente del Comité Empresarial Ecuatoriano
- **Perfil de impacto:** Empresario ecuatoriano con amplia trayectoria en el sector industrial y gremial. Fue designado presidente del Comité Empresarial Ecuatoriano (CEE) para el período 2025–2026, desde donde lidera la representación de más de un centenar de gremios productivos del país y articula la posición del sector privado frente a reformas económicas, laborales y tributarias. Ha ocupado cargos directivos en la Cámara de Industrias de Guayaquil y en empresas con operaciones nacionales e internacionales.
- **Temática clave:** Desarrollo productivo
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Encabeza la principal instancia de representación del sector privado del país. La interlocución permite posicionar a Holcim dentro de la agenda empresarial frente al Gobierno y a las reformas económicas en discusión.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/navarro.jpg`

#### José María Ponce  `[R]`
- **Cargo:** Presidente del Directorio de la Cámara de Industrias y Producción
- **Perfil de impacto:** Empresario ecuatoriano, graduado de Texas Christian University y con maestría en Negocios por la Pontificia Universidad Católica de Chile. Es gerente general de Textiles Texsa desde 2003 y fue presidente de la Asociación de Industriales Textiles del Ecuador. Vinculado a la CIP por más de 15 años, ha sido vicepresidente, presidente y presidente ejecutivo interino del gremio. Desde marzo de 2026 preside su Directorio para el período 2026–2027 y, tras la salida de María Paz Jervis de la presidencia ejecutiva en septiembre de 2026, es la principal voz del gremio.
- **Temática clave:** Industria
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Preside el principal gremio industrial del país, del que Holcim forma parte del tejido productivo. La interlocución permite posicionar la agenda de la industria de la construcción frente a temas de competitividad y abastecimiento energético, en un momento de transición en la conducción del gremio.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/ponce.jpg`

#### Miguel Ángel González  `[R]`
- **Cargo:** Presidente de la Cámara de Comercio de Guayaquil
- **Perfil de impacto:** Economista y empresario ecuatoriano con experiencia en gestión gremial. Fue reelecto presidente de la Cámara de Comercio de Guayaquil para el período 2024–2027, al frente de uno de los gremios más antiguos y numerosos del país, con cerca de 10.000 socios. Ha promovido el libre comercio, la facilitación de negocios y la atracción de inversiones, y ha fortalecido la relación entre el sector privado y las autoridades públicas.
- **Temática clave:** Desarrollo productivo
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Dirige uno de los gremios empresariales más influyentes de Guayaquil, ciudad donde se concentra parte importante de la operación de Holcim. La interlocución permite fortalecer la presencia de la compañía en el ecosistema empresarial de la ciudad.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/gonzalez.jpg`

#### Jorge Yandun  `[R]`
- **Cargo:** Representante de Constructores Positivos
- **Perfil de impacto:** Ingeniero mecánico por la Escuela Politécnica Nacional, con MBA. Empresario e impulsor del sector de la construcción en Ecuador; ha sido presidente ejecutivo de Kubiec, Conduit y Acerogar, empresas industriales vinculadas a la construcción y la metalmecánica. Fue presidente de la Cámara de Comercio de Cuenca y es líder de Constructores Positivos, organización gremial que articuló la eliminación de la Ley de Plusvalía y promovió la reactivación del mercado inmobiliario.
- **Temática clave:** Construcción
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Se ha consolidado como una figura relevante en el sector de la construcción y mantiene cercanía con el Gobierno en temas de política sectorial. La interlocución permite alinear la agenda de Holcim con la de constructores y promotores inmobiliarios, principales demandantes de cemento y hormigón del país.
- **Acompañamiento:** Área Comercial
- **Foto:** `fotos/yandun.jpg`

#### Xavier Rosero Carrillo  `[C]`
- **Cargo:** Presidente Ejecutivo de Fedexpor
- **Perfil de impacto:** Fue vicepresidente ejecutivo de Fedexpor desde 2021 y luego designado presidente ejecutivo, en reemplazo de Felipe Ribadeneira. Ha impulsado misiones comerciales para abrir nuevos mercados, ha respaldado acuerdos comerciales como el de Corea del Sur y ha planteado la necesidad de negociar con Estados Unidos la sobretasa arancelaria a las exportaciones ecuatorianas.
- **Temática clave:** Exportaciones
- **Mecanismo de abordaje:** Comunicación escrita
- **Razonamiento del actor:** Representa al sector exportador del país y tiene incidencia en la agenda de comercio exterior frente al Gobierno. Al no tener una incidencia directa en la operación de Holcim, se recomienda únicamente el envío de una carta de presentación del nuevo CEO para mantener el canal abierto.
- **Acompañamiento:** NA
- **Foto:** `fotos/rosero.jpg`


### Cooperación Internacional – Mes 03

#### Stefan Klötzli  `[R]`
- **Cargo:** Embajador de Suiza en Ecuador
- **Perfil de impacto:** Diplomático de carrera del servicio exterior suizo desde 1998. Se desempeñó como primer secretario en la misión de Suiza en Canberra y como embajador de Suiza en Uzbekistán. En junio de 2025 fue designado Embajador Extraordinario y Plenipotenciario de Suiza en Ecuador. Entre sus prioridades ha señalado la cooperación económica, la innovación, la protección ambiental y el fortalecimiento de las condiciones de inversión, junto con la Cámara de Comercio Suizo-Ecuatoriana (Swisscham).
- **Temática clave:** Relación con Suiza
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Representa al país de origen de Holcim y es el principal canal de la relación bilateral entre Suiza y Ecuador. La interlocución permite fortalecer el respaldo institucional a la compañía y anticipar eventuales riesgos que puedan afectar la inversión suiza en el país.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/klotzli.jpg`

#### Ignez Tristao  `[R]`
- **Cargo:** Representante del BID en Ecuador
- **Perfil de impacto:** Se desempeña como Representante del Banco Interamericano de Desarrollo (BID) en Ecuador, donde lidera la relación institucional con el Gobierno y el sector privado, coordina el portafolio de financiamiento y cooperación técnica, y supervisa la ejecución de proyectos orientados a desarrollo productivo, sostenibilidad fiscal y fortalecimiento institucional. Cuenta con experiencia previa como representante del BID en Guatemala y en gestión de operaciones país en América Latina.
- **Temática clave:** Infraestructura
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Tiene capacidad de incidir en la estructuración de financiamiento y programas de inversión en infraestructura y vivienda en Ecuador. La interlocución permite anticipar las líneas prioritarias de inversión multilateral y posicionar a Holcim en proyectos de construcción sostenible.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/tristao.jpg`

#### Diana Mejía  `[R]`
- **Cargo:** Representante de CAF en Ecuador
- **Perfil de impacto:** Economista con trayectoria en desarrollo productivo, competitividad y fortalecimiento institucional en América Latina. En CAF ha liderado iniciativas vinculadas a productividad, innovación, clima de negocios y apoyo a MIPYMES, articulando financiamiento con asistencia técnica para gobiernos y sector privado. Su trabajo se enfoca en crecimiento sostenible, integración regional y políticas públicas orientadas al desarrollo.
- **Temática clave:** Infraestructura
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Máxima autoridad en el país de un banco multilateral con capacidad de financiar proyectos de infraestructura de largo plazo. La interlocución permite identificar oportunidades en obras financiadas por CAF y en iniciativas de financiamiento verde.
- **Acompañamiento:** Asuntos Corporativos
- **Foto:** `fotos/mejia.jpg`


### Líderes empresariales – Transversal

#### Isabel Noboa  `[C]`
- **Cargo:** Consorcio Nobis
- **Temática clave:** Inversión productiva
- **Foto:** `fotos/noboa.jpg`

#### Andrew Wright  `[C]`
- **Cargo:** Corporación Favorita
- **Temática clave:** Inversión productiva
- **Foto:** `— (silueta)`

#### Santiago Peralta  `[C]`
- **Cargo:** Paccari
- **Temática clave:** Sostenibilidad
- **Foto:** `fotos/peralta.jpg`

#### Roque Sevilla  `[C]`
- **Cargo:** Grupo Futuro
- **Temática clave:** Sostenibilidad
- **Foto:** `fotos/sevilla.jpg`

#### Josué de la Maza  `[C]`
- **Cargo:** Nestlé
- **Temática clave:** Agro
- **Foto:** `fotos/maza.jpg`

#### Michel Deller  `[R]`
- **Cargo:** Presidente del Directorio de DK Management Services
- **Perfil de impacto:** Empresario ecuatoriano con trayectoria en los sectores inmobiliario, comercial y de consumo. Preside el Directorio de DK Management Services, empresa que desarrolla y opera ocho centros comerciales en el país, entre ellos Quicentro Shopping, Quicentro Sur, San Luis Shopping y Portal Shopping, y que impulsa la expansión de San Luis Town Center. Es además conocido por la franquicia de KFC en Ecuador y por sus inversiones en el fútbol, entre ellas Independiente del Valle.
- **Temática clave:** Inmobiliario
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Lidera uno de los principales desarrolladores y operadores de centros comerciales del país y ocupa el puesto 12 del Ranking Merco Líderes 2025. La interlocución permite explorar oportunidades de suministro en sus nuevos proyectos y ampliaciones.
- **Acompañamiento:** Área Comercial
- **Foto:** `fotos/deller.jpg`

#### Pablo Campana  `[R]`
- **Cargo:** Fundador y CEO de Millenium
- **Perfil de impacto:** Ingeniero comercial por Pacific University, con MBA del IMD. Ocupó diversos cargos en Consorcio Nobis, entre ellos la gerencia de Pronobis, y fundó la promotora inmobiliaria Millenium, con proyectos residenciales y corporativos en Quito y Guayaquil. Entre 2017 y 2019 fue ministro de Comercio Exterior y, posteriormente, de Producción, Comercio Exterior, Inversiones y Pesca.
- **Temática clave:** Inmobiliario
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Lidera una de las principales promotoras inmobiliarias del país y, como exministro de Comercio Exterior, mantiene interlocución con el sector público y gremial. La interlocución permite explorar oportunidades de suministro en sus proyectos en Quito y Guayaquil.
- **Acompañamiento:** Área Comercial
- **Foto:** `fotos/campana.jpg`

#### Tommy Schwarzkopf  `[R]`
- **Cargo:** Fundador de Uribe & Schwarzkopf
- **Perfil de impacto:** Empresario de la construcción con más de cinco décadas de trayectoria. En 1973 cofundó, junto al ingeniero civil Bernardo Uribe, la constructora Uribe & Schwarzkopf, una de las principales desarrolladoras inmobiliarias de Quito, reconocida por sus proyectos residenciales en altura diseñados con firmas de arquitectura internacionales. Su subsidiaria Brik cotiza en las bolsas de valores de Quito y Guayaquil.
- **Temática clave:** Inmobiliario
- **Mecanismo de abordaje:** Reunión one-to-one
- **Razonamiento del actor:** Fundador de una de las constructoras más relevantes del país y referente del desarrollo vertical en Quito. La interlocución permite posicionar a Holcim como aliado en soluciones constructivas para proyectos de vivienda en altura.
- **Acompañamiento:** Área Comercial
- **Foto:** `fotos/schwarzkopf.jpg`
