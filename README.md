PhotoCraft

<p align="center">
  <a href="https://getartcraft.com/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="docs/brand/artcraft-logo-white.svg">
      <img alt="ArtCraft" src="docs/brand/artcraft-logo.svg" width="200">
    </picture>
  </a>
</p><p align="center">
  <img src="assets/app-icon/hicolor/256x256/apps/ai.storyteller.photocraft.png" width="128" height="128" alt="Icono de PhotoCraft: un zorro de nueve colas grabado sobre una baldosa azul">
</p><h1 align="center">PhotoCraft</h1><p align="center">
  <b>Edición de imágenes: una reimplementación independiente y de código abierto de Adobe Photoshop, reconstruida íntegramente en Rust.</b><br>
  Capas, máscaras, capas de ajuste, estilos de capa, texto, vectores, pinceles y archivos PSD reales,<br>
  en una aplicación nativa escrita completamente en Rust. Código abierto, sin conexión y bajo tu control.
</p><p align="center">
  <img alt="100 % Rust" src="https://img.shields.io/badge/100%25-Rust-b7410e?style=flat-square&logo=rust">
  <img alt="macOS · Windows · Linux · FreeBSD · Web" src="https://img.shields.io/badge/macOS%20%C2%B7%20Windows%20%C2%B7%20Linux%20%C2%B7%20FreeBSD%20%C2%B7%20Web-native-2f7bf5?style=flat-square">
  <img alt="Licencia: MIT o Apache-2.0" src="https://img.shields.io/badge/license-MIT%20%2F%20Apache--2.0-3a3a3a?style=flat-square">
  <img alt="Estado: versión alfa inicial" src="https://img.shields.io/badge/status-early%20alpha-d69e2e?style=flat-square">
  <br>
  <a href="https://sonarcloud.io/project/overview?id=storytold_photocraft"><img alt="Analizado por SonarCloud" src="https://img.shields.io/badge/Scanned_by-SonarCloud-4b9fd5?style=flat-square&logo=sonarqubecloud&logoColor=white"></a>
  <a href="https://coderabbit.ai"><img alt="Revisado por CodeRabbit" src="https://img.shields.io/coderabbit/prs/github/storytold/photocraft?style=flat-square&label=Revisado%20por%20CodeRabbit&logo=coderabbit"></a>
</p><p align="center">
  <a href="https://discord.gg/artcraft"><img alt="Únete a la comunidad de ArtCraft en Discord" src="https://img.shields.io/badge/Únete%20a%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" height="40"></a>
</p><p align="center">
  <a href="https://getartcraft.com/apps/photocraft"><b>PhotoCraft en getartcraft.com</b></a> ·
  <a href="https://getartcraft.com/">ArtCraft</a> ·
  <a href="https://getartcraft.com/apps">Todas las aplicaciones creativas</a>
</p><br><p align="center">
  <img src="docs/images/photocraft-demo.jpg" alt="PhotoCraft editando La gran ola de Hokusai" width="100%">
  <br>
  <sub>Una tarjeta de texto con sombra, texto editable y capas de ajuste de Intensidad y Curvas, con el editor de Curvas abierto.<br>
  <i>La gran ola de Kanagawa</i>, Katsushika Hokusai, c. 1831</sub>
</p>«[!NOTE]
ArtCraft es una comunidad de artistas de todos los ámbitos. Arte digital, generativo, música, videojuegos... Si creas cosas, formas parte de nosotros. "Ven a saludarnos a Discord" (https://discord.gg/artcraft).»

<p align="center">
  <a href="#características">Características</a> ·
  <a href="#todo-lo-que-incluye">Todo lo que incluye</a> ·
  <a href="#compatibilidad-psd-sin-compromisos">PSD</a> ·
  <a href="#preparado-para-agentes">Agentes</a> ·
  <a href="#funcionamiento-interno">Funcionamiento interno</a> ·
  <a href="#primeros-pasos">Primeros pasos</a> ·
  <a href="#descargas">Descargas</a> ·
  <a href="#aplicaciones-crafting">Aplicaciones Crafting</a> ·
  <a href="https://discord.gg/artcraft">Discord</a>
</p><br><table>
  <tr>
    <td width="25%" valign="top">
      <h3>🎛️ Diseño familiar</h3>
      Los menús, atajos de teclado, paneles y herramientas están donde tus manos esperan encontrarlos, desde ⌘J hasta ⇧⌘D. Si conoces Photoshop, ya sabes utilizar PhotoCraft.
    </td>
    <td width="25%" valign="top">
      <h3>⚡ Nativo y rápido</h3>
      Un compositor GPU basado en wgpu (Metal, Vulkan, DX12 y WebGPU), mosaicos con copia al escribir y filtros multinúcleo. Sin Electron, sin vistas web y sin esperas.
    </td>
    <td width="25%" valign="top">
      <h3>🗂️ Archivos PSD reales</h3>
      Abre, edita y guarda documentos de Photoshop con capas. Al volver a guardar, se conserva la representación visual de 307 de los 309 archivos de prueba de psd-tools.
    </td>
    <td width="25%" valign="top">
      <h3>🤖 Preparado para agentes</h3>
      Cada acción es un comando, por lo que puedes controlar el mismo motor desde la interfaz, la CLI, un canal de control JSON o un servidor MCP.
    </td>
  </tr>
</table><br>Características

Todas las capturas de pantalla de esta sección muestran la aplicación real trabajando con obras de dominio público, renderizadas fuera de pantalla mediante su canal de control.

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-adjustments.jpg" alt="Monet, Impresión, sol naciente, con capas de ajuste de Niveles e Intensidad" width="100%">
      <br>
      <sub>Capas de ajuste de Niveles e Intensidad, con el panel de Histograma en tiempo real.<br><i>Impresión, sol naciente</i>, Claude Monet, 1872</sub>
      <h3>Edita sin arrepentimientos</h3>
      Las capas de ajuste mantienen todas las modificaciones editables. Combina Niveles, Curvas, Intensidad, Tono/Saturación y muchas otras opciones, aplícalas a determinadas áreas mediante máscaras, cambia su orden o desactívalas. Los píxeles originales nunca se modifican.
      <br><br>
      **16 capas de ajuste** que también pueden aplicarse directamente a los píxeles. Incluyen Curvas con edición por canales, Niveles con histograma en tiempo real, Blanco y negro, Mezclador de canales, Mapa de degradado, Filtro de fotografía, Color selectivo y Búsqueda de color (.cube, .3dl, .look). También incluyen Sombras/Iluminaciones, Reemplazar color, Igualar color, Tonalidad HDR, Desaturar e Igualar.
    </td>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-layer-styles.jpg" alt="Ventana de estilos de capa editando un resplandor exterior" width="100%">
      <br>
      <sub>Resplandor exterior y Trazo en una capa de texto editable, dentro del cuadro de estilos de capa.<br><i>Earthrise</i>, William Anders / NASA, 1968</sub>
      <h3>Estilos que realzan tus imágenes</h3>
      Sombra paralela, sombra interior, resplandor exterior e interior, bisel y relieve, satinado, trazo y superposiciones de color, degradado y motivo. Todos pueden aplicarse a cualquier capa, incluso a las de texto.
      Los motivos proceden de una biblioteca (incluye los integrados, Editar › Definir motivo e importación/exportación de archivos <code>.pat</code>) y de los bloques PSD <code>Patt</code>.
      <br><br>
      Copia y pega estilos entre capas, oculta todos los efectos a la vez y abre directamente los estilos de tus archivos PSD, con un resultado visual que busca coincidir con Photoshop.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-masks.jpg" alt="La joven de la perla de Vermeer con selección elíptica y máscara de Tono y Saturación" width="100%">
      <br>
      <sub>Una selección elíptica se convierte en la máscara de una capa de Tono/Saturación, de modo que solo el rostro conserva su color.<br><i>La joven de la perla</i>, Johannes Vermeer, c. 1665</sub>
      <h3>Selecciones que entienden tus imágenes</h3>
      Herramientas de marco, lazos y Varita mágica para realizar selecciones precisas. Selección rápida, Selección de objetos y Seleccionar sujeto cuando quieras que el ordenador realice el trazado automáticamente. Seleccionar y aplicar máscara permite perfeccionar incluso los bordes más delicados del cabello.
      <br><br>
      Suaviza, expande, contrae, mejora o vuelve a seleccionar. Convierte cualquier selección en una máscara de capa, un trazado vectorial o una forma. Las selecciones inteligentes se procesan en tu propio dispositivo, sin servicios en la nube ni necesidad de crear una cuenta.
    </td>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-type.jpg" alt="Texto editándose sobre una imagen de Albert Bierstadt" width="100%">
      <br>
      <sub>Un titular editado directamente sobre el lienzo, acompañado de una firma y un párrafo.<br><i>Entre las montañas de Sierra Nevada, California</i>, Albert Bierstadt, 1868</sub>
      <h3>Texto con acabado profesional</h3>
      Texto de punto y de párrafo, editable directamente sobre el lienzo, con controles completos de Carácter y Párrafo: fuente, grosor, tamaño, interlineado, espaciado, alineación y color. El <a href="docs/color-picker.md">selector completo de color de texto</a> también permite tomar muestras de la pantalla con una lupa de píxeles.
      <br><br>
      Las capas de texto permanecen editables, admiten estilos de capa y son compatibles con la importación y exportación PSD.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-vector.jpg" alt="Insignia de loto creada con capas de formas vectoriales" width="100%">
      <br>
      <sub>Una insignia formada por capas: un loto con relleno degradado, una estrella y un anillo punteado.<br><i>Los nenúfares</i>, Claude Monet, 1906</sub>
      <h3>Vectores con precisión de píxel</h3>
      Herramientas Rectángulo, Elipse, Triángulo, Polígono, Línea y Pluma, Pluma de forma libre y Pluma de curvatura. Incluye capas de formas independientes de la resolución, rellenos degradados y trazos discontinuos y alineados.
      <br><br>
      Combina formas (unir, restar, intersecar y excluir), guarda trazados en el panel Trazados, utilízalos como máscaras vectoriales o aplica trazos y rellenos. Las 116 capas de formas de nuestro conjunto de pruebas PSD coinciden píxel a píxel con Photoshop.
    </td>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-filters.jpg" alt="Filtro de giro aplicado a La noche estrellada de Van Gogh" width="100%">
      <br>
      <sub>El filtro Giro muestra una vista previa en tiempo real sobre el lienzo, únicamente dentro de la selección.<br><i>La noche estrellada</i>, Vincent van Gogh, 1889</sub>
      <h3>Visualiza antes de aplicar</h3>
      Todos los cuadros de diálogo de filtros muestran una vista previa en tiempo real sobre el lienzo, respetando las selecciones.  Incluye desenfoques (gaussiano, de cuadro, de movimiento, radial, de superficie, inteligente, de lente y de forma, además de la Galería de desenfoques: Desplazamiento de inclinación, Iris, Campo, Giro y Trazado), enfoque, reducción de ruido, distorsiones (Giro, Onda, Rizo, Desplazar, Distorsionar, Zigzag...), pixelización, estilización (Pintura al óleo, Viento, Extrusión...), renderizado (Nubes, Fibras, Destello de lente, Efectos de iluminación) y mucho más.
  <br><br>
  Si aplicas filtros a un objeto inteligente, estos permanecen editables: puedes modificarlos, ocultarlos, cambiar su orden o aplicarles máscaras en cualquier momento.
  <br><br>
  Los desenfoques de gran radio utilizan pasadas de suma acumulada en todos los núcleos. Un desenfoque gaussiano de radio 180 sobre 3,6 megapíxeles tarda menos de un segundo.
</td>

  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-transform.jpg" alt="Transformación libre de una imagen de Ansel Adams con el panel Historial abierto" width="100%">
      <br>
      <sub>Transformación libre de una impresión girada, con cada paso registrado en el Historial.<br><i>Los Tetons y el río Snake</i>, Ansel Adams, 1942</sub>
      <h3>Da forma a tus imágenes como quieras</h3>
      Transformación libre con escala, rotación, inclinación, distorsión y perspectiva. Rotaciones exactas de 90° y 180°, volteo y opción de repetir transformación. Las capas, textos, formas, máscaras y selecciones se transforman conjuntamente.
      <br><br>
      El historial completo, Alternar último estado y el Pincel de historia permiten deshacer cualquier paso, incluso pincelada por pincelada.
    </td>
    <td width="50%" valign="top">
      <img src="docs/images/photocraft-export-light.jpg" alt="Ventana Exportar como con una imagen de Klimt" width="100%">
      <br>
      <sub>Exportar como en el tema claro, con vista previa y estimación del tamaño del archivo.<br><i>El beso</i>, Gustav Klimt, 1907–1908</sub>
      <h3>Exporta tus trabajos a cualquier lugar</h3>
      Exportar como permite elegir el formato, la calidad, la transparencia y la escala, además de mostrar una vista previa y una estimación instantánea del tamaño del archivo. También incluye Exportación rápida a PNG con un solo clic.
      <br><br>
      Elige entre un tema oscuro Pro, los temas claros Studio o una apariencia clásica.
    </td>
  </tr>
</table><br>Todo lo que incluye

<table>
  <tr>
    <td width="33%" valign="top">
      <h4>🧰 68 herramientas</h4>
      Mover · Mesa de trabajo · Marco rectangular y elíptico · Marco de fila única · Marco de columna única · Lazo · Lazo poligonal · Lazo magnético · Selección de objetos · Selección rápida · Varita mágica · Recortar · Recorte con perspectiva · Sector · Seleccionar sector · Marco · Cuentagotas · Muestra de color · Regla · Nota · Contar · Quitar · Pincel corrector puntual · Pincel corrector · Parche · Movimiento según contenido · Ojos rojos · Pincel · Lápiz · Pincel mezclador · Sustitución de color · Tampón de clonar · Tampón de motivo · Pincel de historia · Pincel histórico artístico · Borrador · Borrador de fondos · Borrador mágico · Degradado · Bote de pintura · Desenfocar · Enfocar · Dedo · Sobreexponer · Subexponer · Esponja · Pluma · Pluma de forma libre · Pluma de curvatura · Añadir punto de ancla · Eliminar punto de ancla · Convertir punto · Texto horizontal y vertical · Máscara de texto horizontal y vertical · Selección de trazado · Selección directa · Rectángulo · Elipse · Triángulo · Polígono · Línea · Forma personalizada · Mano · Rotar vista · Zoom.
    </td>
    <td width="33%" valign="top">
      <h4>🖌️ Un motor de pinceles real</h4>
      Dinámica de forma, dispersión, textura, pincel doble, dinámica de color, transferencia, posición del pincel, bordes húmedos, acumulación y suavizado (incluido el modo Cuerda tensada).  Compatible con presión, inclinación, rotación y dirección del lápiz digital. Incluye ajustes preestablecidos de pincel, creación de pinceles desde selecciones y trazos deterministas que pueden reproducirse.
</td>
<td width="33%" valign="top">
  <h4>🗃️ Capas bien implementadas</h4>
  Grupos, máscaras de recorte, máscaras de píxeles y vectoriales, capas de relleno (sólido, degradado y motivo), capas de ajuste, objetos inteligentes editables con filtros inteligentes y transformaciones y deformaciones sin pérdida.

  Selección de varias capas con alineación, distribución y vinculación, canales alfa y Máscara rápida, 27 modos de fusión de Photoshop más seis variantes de Paint.NET, opacidad y relleno, bloqueos, etiquetas de color, filtro por tipo de capa, combinar, acoplar, rasterizar, Capa mediante copia/corte y Pegar dentro.
</td>

  </tr>
  <tr>
    <td width="33%" valign="top">
      <h4>🎨 Cualquier color y profundidad</h4>
      Documentos RGB, escala de grises, CMYK y Lab a 8, 16 y 32 bits por canal. La profundidad de bits y el modelo de color son datos dinámicos, por lo que todas las herramientas funcionan con cualquier profundidad.
      <br><br>
      Gestión real del color ICC completamente en Rust: perfiles incrustados, Asignar y Convertir a perfil con los cuatro métodos de representación y compensación de punto negro, prueba de color en pantalla (⌘Y) y advertencia de gama (⇧⌘Y) mediante GPU.
    </td>
    <td width="33%" valign="top">
      <h4>🗂️ Formatos compatibles</h4>
      PSD y PSB; TIFF con capas (datos de capas de Photoshop dentro del TIFF, con lectura y escritura en ambos órdenes de bytes); <a href="docs/pdn.md">Paint.NET PDN3 (lectura, con capas editables y sus 14 modos de fusión)</a>; <a href="docs/ora.md">OpenRaster (lectura y escritura, con capas, grupos y modos de fusión para Krita, MyPaint y GIMP)</a>; <a href="docs/xcf.md">GIMP XCF (lectura, con capas, grupos, máscaras, modos de fusión, canales y selección)</a>; <a href="docs/kra.md">Krita .kra (lectura, con capas de pintura, grupos, modos de fusión y máscaras de transparencia)</a>; SVG (se abre como capas de formas y se inserta como objeto inteligente vectorial).  También admite PNG, JPEG, TIFF, WebP (con y sin pérdida), GIF, BMP, TGA, ICO, QOI, PNM, OpenEXR, Radiance HDR y FITS (imágenes astronómicas: 8/16 bits y coma flotante de 32 bits, en escala de grises o RGB, conservando la cabecera), además del formato nativo <code>.pcraft</code>.
  
  Los formatos planos conservan las profundidades que admiten: PNG conserva muestras de 8/16 bits, TIFF conserva muestras de 8/16 bits y coma flotante de 32 bits, y OpenEXR conserva muestras de media y coma flotante. JPEG, WebP y los demás formatos de 8 bits reducen las muestras de mayor profundidad y muestran una advertencia durante la exportación.
  
  Consulta la <a href="crates/codecs/README.md#capability-matrix-default-build">tabla de compatibilidad de formatos</a> para conocer los detalles.
  
  Las fotografías HEIC de iPhone y Mac se pueden abrir en modo de solo lectura (incluidas en las versiones oficiales; las compilaciones desde el código fuente pueden activar opcionalmente <code>--features heif</code>).
  
  AVIF solo está disponible para escritura mediante la característica opcional de compilación <code>avif</code>. La decodificación AVIF y JPEG XL no están disponibles.
  
  Los documentos de Affinity (<code>.af</code>, <code>.afdesign</code>, <code>.afphoto</code>, <code>.afpub</code>) se abren de forma nativa en modo de solo lectura, con mesas de trabajo, capas, vectores, texto, imágenes y máscaras. Los efectos, ajustes y otros elementos no compatibles aparecen en una advertencia. La exportación a formatos de Affinity no está disponible.
</td>
<td width="33%" valign="top">
  <h4>🪄 Herramientas esenciales para el día a día</h4>
  Tono automático, Contraste automático y Color automático · Igualar · Tamaño de imagen y lienzo · Recortar y ajustar · Mostrar todo · Editar › Rellenar y Trazo · Copiar combinado · Pegar en el mismo lugar · Guías, reglas, cuadrícula y ajuste · Grabación y reproducción de acciones · Paleta de comandos (⌘F).
</td>

  </tr>
</table><br>Compatibilidad PSD sin compromisos

La compatibilidad PSD de PhotoCraft es un módulo independiente, desarrollado a partir de la especificación pública de Adobe y probado con una colección de archivos reales.

- Importación y exportación fieles: abrir y volver a guardar un documento produce el mismo resultado visual en 307 de los 309 archivos del conjunto de pruebas de psd-tools y en 169 de los 170 archivos de nuestro conjunto combinado ag-psd/psd-tools ("crates/io/tests/it/corpus.rs"; descarga el conjunto de psd-tools con "cargo xtask corpus --psd-tools"). Los elementos que todavía no modelamos (bloques sin procesar, descriptores y datos adicionales) se conservan en lugar de descartarse. Un archivo guardado nuevamente no es idéntico byte por byte al original: PhotoCraft reescribe los recursos de imagen, los registros de capas y la composición final. Solo el módulo independiente "photocraft-psd", que analiza y escribe archivos sin utilizar el modelo de documento, reproduce byte por byte todos los archivos analizables del conjunto de pruebas ("crates/psd/tests/it/corpus.rs").
- Píxeles coincidentes: un sistema de comparación contrasta nuestro resultado con la imagen combinada generada por el propio Photoshop. Incluye interpolación de degradados (Clásica, Perceptual y Lineal), efectos de capa, trazos de formas, recortes y opacidad de relleno.
- Documentos grandes: compatibilidad nativa con PSB, archivos de 16 y 32 bits, y documentos CMYK y Lab.

Preparado para agentes

Cada elemento de menú, herramienta y cuadro de diálogo ejecuta un comando de un registro común con más de 500 comandos.

La interfaz gráfica, la CLI, el canal de control JSON y el servidor MCP utilizan los mismos comandos. Esto significa que cualquier acción que puedas realizar con un clic también puede ejecutarse mediante un script o un agente de inteligencia artificial.

# Sin interfaz gráfica: abrir, editar y guardar
photocraft-cli run wave.psd \
  --cmd filter.sharpen.smartSharpen     --params '{"amount":80}' \
  --cmd layer.newAdjustmentLayer.curves --params '{"points":[[0,0],[64,48],[192,212],[255,255]]}' \
  --out wave-final.png

# Aplicar una lista de acciones a una carpeta de imágenes
photocraft-cli batch --actions grade.json --in ./raw --out ./graded

# Cada subcomando explica cómo utilizarse
photocraft-cli batch --help

# Permitir que un agente controle la aplicación mediante MCP
photocraft-cli mcp

La aplicación de escritorio también ofrece un canal de control autenticado y limitado a conexiones locales ("photocraft --control"). Permite inspeccionar el estado de la interfaz, controlar herramientas mediante eventos de puntero y realizar capturas fuera de pantalla.

Todas las imágenes de este README se generaron de esa manera. Consulta ""docs/control-protocol.md"" (docs/control-protocol.md).

Funcionamiento interno

- Motor como prioridad: un modelo de documento basado en datos y un motor de comandos, con una interfaz egui ligera. La arquitectura se organiza en 24 módulos independientes.
- Dos compositores: un compositor CPU sirve como referencia de comparación, mientras que un compositor wgpu utiliza la GPU para representar el lienzo. Ambos se prueban entre sí.
- Mosaicos con copia al escribir: mosaicos dispersos de 256² permiten realizar deshacer de forma económica y mantener ligeros los lienzos enormes. Los mapas de efectos se almacenan en caché según el estado de cada capa.
- Funciona en el navegador: todo el motor y la interfaz pueden compilarse a WebAssembly.
- Desarrollo independiente: implementado únicamente a partir de especificaciones públicas y comportamientos observados. No utiliza código, sombreadores ni recursos propietarios.
- Probado: más de 1.700 pruebas, incluidas pruebas de importación/exportación PSD, generadores sintéticos, comparaciones de composición y comprobaciones de múltiples profundidades.

Primeros pasos

git clone https://github.com/storytold/photocraft
cd photocraft
cargo run --release -p photocraft -- image.psd   # aplicación de escritorio
cargo test --workspace                           # ejecutar las pruebas

Las fuentes japonesas de la interfaz y de la herramienta Texto proceden de "craft-fonts" (https://github.com/storytold/craft-fonts), una dependencia de compilación opcional (las versiones oficiales de escritorio siempre las incluyen). Sin ellas, PhotoCraft utiliza las fuentes CJK disponibles en el sistema:

git clone https://github.com/storytold/craft-fonts ../craft-fonts
CRAFT_FONTS_DIR="$PWD/../craft-fonts" cargo run --release -p photocraft

Para nuevos colaboradores y agentes de inteligencia artificial: comienza leyendo ""AGENTS.md"" (AGENTS.md) y después consulta ""docs/"" (docs/).

Los instaladores para macOS, Windows, Linux, FreeBSD y la versión web están disponibles en cada "lanzamiento de GitHub" (https://github.com/storytold/photocraft/releases).

En Linux puedes elegir entre AppImage, ".deb", ".rpm", un archivo comprimido tarball o un paquete Flatpak. El paquete necesita el entorno de ejecución de freedesktop desde "Flathub" (https://flathub.org/setup), que Flatpak puede instalar junto con la aplicación:

flatpak install --user photocraft-<version>-linux-x86_64.flatpak   # o -linux-aarch64
flatpak run ai.storyteller.photocraft

Flatpak imprime mediante el socket CUPS del sistema anfitrión (Archivo › Imprimir se comunica directamente mediante IPP, sin necesidad de "lp"). Si CUPS no está instalado o no hay ninguna impresora disponible, Archivo › Imprimir abre el cuadro de diálogo de impresión del sistema mediante el portal de impresión.

Consulta "impresión" (docs/printing.md).

AppImage no necesita instalación. La primera ejecución registra el icono del lanzador y la entrada del menú en "~/.local/share", de modo que el dock muestre el icono de PhotoCraft en Wayland.

Establece "PHOTOCRAFT_NO_DESKTOP_INTEGRATION=1" para omitir esta integración. Consulta ""docs/releasing.md"" (docs/releasing.md) › Linux para deshacerla.

Para utilizar la CLI incluida, ejecuta:

./photocraft-<version>-linux-x86_64.AppImage --cli --help

También puedes utilizar "--cli mcp" para iniciar el servidor MCP mediante entrada y salida estándar. Los lanzamientos de la CLI omiten la integración con el escritorio.

Un enlace simbólico llamado "photocraft-cli" también permite seleccionar la CLI. Consulta ""docs/development.md"" (docs/development.md#headless-cli).

En sesiones Wayland, todavía no es posible abrir archivos arrastrándolos directamente sobre la ventana: winit 0.30, la biblioteca de ventanas utilizada por egui, aún no admite esta función en Wayland (#386).

Como alternativa, utiliza Archivo › Abrir o copia la imagen desde el administrador de archivos y pégala con Ctrl+V.

Para arrastrar y soltar archivos, inicia PhotoCraft mediante XWayland:

WAYLAND_DISPLAY= photocraft

O utiliza:

WAYLAND_DISPLAY= ./photocraft-<version>-linux-x86_64.AppImage

También puedes ejecutar:

flatpak run --nosocket=wayland --socket=x11 ai.storyteller.photocraft

En Wayland, PhotoCraft muestra una notificación con el comando correspondiente a tu instalación hasta que la descartes.

La opción Preferencias › Rendimiento › Servidor de pantalla de Linux = X11 realiza lo mismo en cada inicio.

Con escalado fraccional de pantalla (125 %, 150 % o 175 %), una ventana XWayland se dibuja a una resolución inferior y después el compositor la amplía, por lo que la interfaz puede verse borrosa. Wayland nativo mantiene la imagen nítida (#1072).

En macOS, la herramienta de línea de comandos se distribuye como "photocraft-cli-<version>-macos-universal.zip".

El binario está firmado con el mismo certificado Developer ID que la aplicación y cuenta con notarización de Apple.

Un binario independiente no puede incluir un ticket de notarización adherido como ocurre con el archivo DMG, por lo que macOS comprueba la notarización en línea la primera vez que se ejecuta.

Puedes verificarlo tú mismo:

ditto -x -k photocraft-cli-<version>-macos-universal.zip .
spctl --assess --type install -vv photocraft-cli-<version>-macos-universal/photocraft-cli
# ... accepted, source=Notarized Developer ID

En FreeBSD 14 (x86_64), la versión se distribuye en un archivo tarball organizado como "/usr/local".

Instala las bibliotecas necesarias y después descomprime el paquete:

pkg install libxkbcommon wayland libX11 libXcursor libXrandr libXi libxcb mesa-libs vulkan-loader gtk3 fontconfig freetype2 alsa-lib
tar -xzf photocraft-<version>-freebsd-x86_64.tar.gz --strip-components 1 -C /usr/local
photocraft

Para los mantenedores: ""docs/releasing.md"" (docs/releasing.md) explica cómo se crean, firman y publican las versiones.

«[!IMPORTANT]
Estado del proyecto: PhotoCraft se encuentra en una fase alfa inicial. Queremos ser transparentes sobre su situación actual: muchas de las funciones de Photoshop ya existen de alguna forma, pero todavía no es un sustituto completo de Photoshop para el trabajo profesional diario.

Sus principales limitaciones son las funciones de inteligencia artificial y generación, 15 herramientas todavía pendientes, la profundidad de las funciones tipográficas y los flujos de trabajo profesionales, además de la compatibilidad con complementos.

Todos los elementos de los menús de Photoshop están conectados a un comando (""docs/parity-checklist.md"" (docs/parity-checklist.md)), pero eso mide su integración, no su comportamiento completo.

Para conocer la situación real, función por función, y los próximos objetivos, consulta la "hoja de ruta" (ROADMAP.md) y la "evaluación de compatibilidad" (docs/target-app-parity.md).

Es posible que encuentres algunos errores o funciones incompletas. Si encuentras problemas, crea un informe e incluye tu sistema operativo, tamaño del documento, número de capas y una captura de pantalla. También puedes informar de los problemas en "Discord" (https://discord.gg/artcraft).»

Paquetes de la comunidad

Estos instaladores son mantenidos por miembros de la comunidad y no por el equipo de PhotoCraft.

En Gentoo, la superposición "::snakebyte overlay" (https://github.com/switch87/snakebyte-overlay) distribuye la versión de Linux como "media-gfx/photocraft-bin":

eselect repository add snakebyte git https://github.com/switch87/snakebyte-overlay.git
emaint sync -r snakebyte
echo 'media-gfx/photocraft-bin ~amd64' >> /etc/portage/package.accept_keywords/photocraft
emerge --ask media-gfx/photocraft-bin

Documentación

La documentación para desarrolladores, arquitectura, automatización, formatos y seguridad se mantiene en el "libro de documentación de PhotoCraft" (book/).

Para alojar tu propia versión web mediante Docker, consulta "Alojamiento web con Docker" (packaging/web/README.md#docker).

Seguridad

La arquitectura de seguridad, el modelado de amenazas, el fortalecimiento del analizador, las pruebas de fuzzing y la comunicación de vulnerabilidades se explican en la "documentación de seguridad" (book/src/security/) y en la "política de seguridad del repositorio" (SECURITY.md).

Conjuntos de pruebas

PhotoCraft se prueba con archivos reales: nuestros propios documentos PSD creados con Photoshop, disponibles en "photocraft-corpus" (https://github.com/storytold/photocraft-corpus), además de los conjuntos psd-tools, ag-psd y PngSuite, fijados y verificados mediante SHA-256.

Descárgalos con:

cargo xtask corpus --all

Ejecuta las pruebas con:

cargo xtask test-corpus

Encontrarás más información en "docs/development.md" (docs/development.md#test-corpora).

Descargas

¿Eres nuevo en PhotoCraft? Descárgalo desde la "página oficial de PhotoCraft en getartcraft.com" (https://getartcraft.com/apps/photocraft). Es la forma más sencilla de instalarlo.

¿Buscas una versión o formato específico? En GitHub, la "última versión" (https://github.com/storytold/photocraft/releases/latest) contiene todos los paquetes disponibles. En "todas las versiones" (https://github.com/storytold/photocraft/releases) encontrarás ediciones anteriores y sus respectivas notas.

"<ver>" en los nombres de los archivos representa el número de versión. El archivo "SHA256SUMS.txt" contiene las sumas de verificación de cada descarga.

Windows

Compilación| Instalador| Versión portable
x64 (Intel/AMD de 64 bits)| "photocraft-<ver>-windows-x64.msi"| "photocraft-<ver>-windows-x64-portable.zip"
arm64 (Snapdragon y otros PC ARM)| "photocraft-<ver>-windows-arm64.msi"| "photocraft-<ver>-windows-arm64-portable.zip"
x86 (32 bits)| "photocraft-<ver>-windows-x86.msi"| "photocraft-<ver>-windows-x86-portable.zip"

Los instaladores y ejecutables cuentan con firma digital de código.

macOS

Compilación| Archivo| Información
Aplicación universal (Apple Silicon e Intel)| "photocraft-<ver>-macos-universal.dmg"| Firmada y notarizada
Herramienta de línea de comandos universal| "photocraft-cli-<ver>-macos-universal.zip"| Firmada y notarizada

Linux

Formato| x86_64| aarch64 (ARM64)| Información
AppImage| "photocraft-<ver>-linux-x86_64.AppImage"| "photocraft-<ver>-linux-aarch64.AppImage"| Funciona en cualquier distribución; actualizaciones mediante "AppImageUpdate" (https://github.com/AppImageCommunity/AppImageUpdate) (archivos ".zsync")
Flatpak| "photocraft-<ver>-linux-x86_64.flatpak"| "photocraft-<ver>-linux-aarch64.flatpak"| Aislado; instalación mediante "flatpak install --user <file>"
Debian/Ubuntu| "photocraft-<ver>-linux-x86_64.deb"| "photocraft-<ver>-linux-aarch64.deb"| 
Fedora/RHEL/openSUSE| "photocraft-<ver>-linux-x86_64.rpm"| "photocraft-<ver>-linux-aarch64.rpm"| 
Archivo comprimido| "photocraft-<ver>-linux-x86_64.tar.gz"| "photocraft-<ver>-linux-aarch64.tar.gz"| Se puede descomprimir en cualquier ubicación

RISC-V (riscv64): únicamente "photocraft-<ver>-linux-riscv64.tar.gz", compilado para Ubuntu 24.04 (requiere glibc 2.39 o superior).

FreeBSD

Compilación| Archivo
x86_64| "photocraft-<ver>-freebsd-x86_64.tar.gz"

Web (WebAssembly)

Compilación| Archivo| Información
Sitio web estático| "photocraft-web-<ver>.zip"| Funciona en navegadores modernos y puede alojarse en cualquier servidor estático

Aplicaciones Crafting

PhotoCraft forma parte de las Crafting Apps: herramientas creativas gratuitas y de código abierto desarrolladas por el equipo de "ArtCraft" (https://getartcraft.com/). Cada aplicación está escrita desde cero en Rust y puede funcionar de manera independiente.

| Aplicación| Función principal| Código fuente| Más información
<img src="https://raw.githubusercontent.com/storytold/photocraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.photocraft.png" alt="" width="32" height="32">| PhotoCraft| Edición de imágenes: capas, máscaras, texto y archivos PSD reales| "GitHub" (https://github.com/storytold/photocraft)| "Sitio web" (https://getartcraft.com/apps/photocraft)
<img src="https://raw.githubusercontent.com/storytold/vectorcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.vectorcraft.png" alt="" width="32" height="32">| VectorCraft| Ilustración vectorial| "GitHub" (https://github.com/storytold/vectorcraft)| "Sitio web" (https://getartcraft.com/apps/vectorcraft)
<img src="https://raw.githubusercontent.com/storytold/filmcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.filmcraft.png" alt="" width="32" height="32">| FilmCraft| Edición de vídeo, color y sonido| "GitHub" (https://github.com/storytold/filmcraft)| "Sitio web" (https://getartcraft.com/apps/filmcraft)
<img src="https://raw.githubusercontent.com/storytold/lightcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.lightcraft.png" alt="" width="32" height="32">| LightCraft| Biblioteca fotográfica y revelado RAW| "GitHub" (https://github.com/storytold/lightcraft)| "Sitio web" (https://getartcraft.com/apps/lightcraft)
<img src="https://raw.githubusercontent.com/storytold/pdfcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.pdfcraft.png" alt="" width="32" height="32">| PdfCraft| Lectura, organización y protección de archivos PDF| "GitHub" (https://github.com/storytold/pdfcraft)| "Sitio web" (https://getartcraft.com/apps/pdfcraft)
<img src="https://raw.githubusercontent.com/storytold/effectcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.effectcraft.png" alt="" width="32" height="32">| EffectCraft| Gráficos en movimiento y efectos visuales| "GitHub" (https://github.com/storytold/effectcraft)| "Sitio web" (https://getartcraft.com/apps/effectcraft)
<img src="https://raw.githubusercontent.com/storytold/designcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.designcraft.png" alt="" width="32" height="32">| DesignCraft| Diseño de páginas y publicación| "GitHub" (https://github.com/storytold/designcraft)| "Sitio web" (https://getartcraft.com/apps/designcraft)
<img src="https://raw.githubusercontent.com/storytold/figcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.figcraft.png" alt="" width="32" height="32">| FigCraft| Diseño de interfaces y creación de prototipos| "GitHub" (https://github.com/storytold/figcraft)| "Sitio web" (https://getartcraft.com/apps/figcraft)
<img src="https://raw.githubusercontent.com/storytold/wordcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.wordcraft.png" alt="" width="32" height="32">| WordCraft| Procesamiento de textos y documentos| "GitHub" (https://github.com/storytold/wordcraft)| "Sitio web" (https://getartcraft.com/apps/wordcraft)
<img src="https://raw.githubusercontent.com/storytold/soundcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.soundcraft.png" alt="" width="32" height="32">| SoundCraft| Grabación y edición de audio| "GitHub" (https://github.com/storytold/soundcraft)| "Sitio web" (https://getartcraft.com/apps/soundcraft)
<img src="https://raw.githubusercontent.com/storytold/deckcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.deckcraft.png" alt="" width="32" height="32">| DeckCraft| Presentaciones y diapositivas| "GitHub" (https://github.com/storytold/deckcraft)| "Sitio web" (https://getartcraft.com/apps/deckcraft)
<img src="https://raw.githubusercontent.com/storytold/cadcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.cadcraft.png" alt="" width="32" height="32">| CADCraft| Diseño asistido por ordenador en 3D| "GitHub" (https://github.com/storytold/cadcraft)| "Sitio web" (https://getartcraft.com/apps/cadcraft)
<img src="https://raw.githubusercontent.com/storytold/gridcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.gridcraft.png" alt="" width="32" height="32">| GridCraft| Hojas de cálculo y datos| "GitHub" (https://github.com/storytold/gridcraft)| "Sitio web" (https://getartcraft.com/apps/gridcraft)
<img src="https://raw.githubusercontent.com/storytold/texturecraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.texturecraft.png" alt="" width="32" height="32">| TextureCraft| Pintura de texturas 3D| "GitHub" (https://github.com/storytold/texturecraft)| "Sitio web" (https://getartcraft.com/apps/texturecraft)
<img src="https://raw.githubusercontent.com/storytold/craft-anything/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.craft-anything.png" alt="" width="32" height="32">| Craft Anything| Descubre cómo funciona cualquier software y crea el tuyo propio| "GitHub" (https://github.com/storytold/craft-anything)| "Sitio web" (https://getartcraft.com/apps/craft-anything)
<img src="https://raw.githubusercontent.com/tangency-labs/solidcraft/main/assets/icons/app/linux/exports/hicolor/64x64/apps/io.tangencylabs.solidcraft.png" alt="" width="32" height="32">| SolidCraft| Diseño CAD paramétrico en 3D de Tangency Labs (aplicación de la comunidad)| "GitHub" (https://github.com/tangency-labs/solidcraft)| 

Y también "ArtCraft" (https://getartcraft.com/), nuestro estudio de inteligencia artificial para crear imágenes y vídeos, diseñado para artistas que desean tener un control real sobre sus creaciones.

Todas las Crafting Apps comparten los mismos principios: desarrollo independiente, código puro en Rust, aplicaciones nativas para macOS, Windows y Linux, funcionamiento en el navegador mediante WebAssembly y compatibilidad completa con agentes.

<br><p align="center">
  <a href="https://discord.gg/artcraft"><img alt="Únete a la comunidad de ArtCraft en Discord" src="https://img.shields.io/badge/Únete%20a%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" height="40"></a>
</p><h3 align="center">Ven a crear con nosotros</h3><p align="center">
  Nuestro Discord es el punto de encuentro de artistas de todo tipo: personas que pintan, fotografían, dibujan, editan películas, diseñan textos y también quienes todavía están descubriendo qué les gusta crear.
  Comparte tus proyectos, pide ayuda, informa de errores o cuéntanos qué funciones te gustaría que tuvieran estas herramientas.
  Sea cual sea tu especialidad y tu experiencia, eres bienvenido.
</p><p align="center">
  <a href="https://discord.gg/artcraft"><b>discord.gg/artcraft</b></a> ·
  <a href="https://getartcraft.com/">getartcraft.com</a> ·
  <a href="https://getartcraft.com/apps">Aplicaciones Crafting</a> ·
  <a href="https://getartcraft.com/apps/photocraft">PhotoCraft</a>
</p>---

Licencia y créditos

PhotoCraft se distribuye bajo una licencia dual: "MIT" (LICENSE-MIT) o "Apache-2.0" (LICENSE-APACHE), a elección del usuario.

Copyright (c) 2026 ArtCraft Team y los colaboradores de PhotoCraft. Los avisos legales obligatorios se encuentran en "NOTICE" (NOTICE).

Las fuentes, iconos, imágenes y otros recursos incluidos mantienen sus propias licencias de código abierto. Cada uno aparece identificado con su autor, origen y licencia en "ATTRIBUTION.md" (ATTRIBUTION.md).

Todas las obras mostradas son de dominio público (Wikimedia Commons, NASA y Archivos Nacionales de Estados Unidos). Las fuentes están disponibles en ""docs/images/SOURCES.md"" (docs/images/SOURCES.md).

El nombre ArtCraft, su marca denominativa y sus logotipos ubicados en ""docs/brand/"" (docs/brand/) son marcas registradas del equipo ArtCraft y no están cubiertos por esta licencia.

Solo pueden utilizarse sin modificaciones y como parte de este repositorio y PhotoCraft, de acuerdo con ""docs/brand/LICENSE-brand.txt"" (docs/brand/LICENSE-brand.txt).

Las bifurcaciones del proyecto (forks) y las versiones modificadas deben eliminar estas marcas.

<sub>Adobe, Photoshop, Illustrator, Premiere Pro, Lightroom, Acrobat, After Effects e InDesign son marcas comerciales o marcas registradas de Adobe Inc. en Estados Unidos y otros países. PhotoCraft es un proyecto independiente y de código abierto que no está afiliado, patrocinado ni respaldado por Adobe Inc. Estos nombres se utilizan únicamente para describir los flujos de trabajo con los que es compatible.</sub>

<p align="center">
  <a href="https://getartcraft.com/"><img alt="ArtCraft" src="docs/brand/artcraft-mark.svg" width="28"></a><br>
  <sub>Creado por el equipo y la comunidad de <a href="https://getartcraft.com/">ArtCraft</a>.</sub>
</p>Historial de estrellas

""Gráfico del historial de estrellas" (https://api.star-history.com/svg?repos=storytold/photocraft&type=Date&legend=top-left)" (https://www.star-history.com/?repos=storytold%2Fphotocraft&type=date&legend=top-left)
