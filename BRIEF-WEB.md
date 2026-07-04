# 🌐 BRIEF WEB — PAÑALERA RUTA 8

> Documento a medida para construir la web de Pañalera Ruta 8 **sin nada genérico**, enfocada en público **+40**.
> Se completa con 15 rondas de 4 preguntas. Cada respuesta queda registrada acá para que la web sea 100% fiel al negocio.

## Contexto del negocio (ya sabido)
- **Qué es:** ⚠️ **MAYORISTA** de pañales (bebé, adulto, juvenil) en San Martín, GBA — vende al **PRECIO DE FÁBRICA**, NO es la fábrica en sí. En toda la web: "mayorista / precio de fábrica", nunca "somos la fábrica / fabricamos / producto propio".
- **A quién vende:** consumidor final (minorista), almacenes, mayoristas, geriátricos, revendedores — precios por segmento.
- **Diferencial de fondo:** precio de fábrica, sin intermediarios.
- **Ecosistema ya construido:** base de datos + panel admin + bot de atención WhatsApp + automatizaciones. La web se enchufa a esa misma base (clientes/pedidos/pagos con canal='web').

---

## Respuestas del discovery (se llena por ronda)

### Ronda 1 — Objetivo, público y tono
- **Objetivo #1:** Vender online (catálogo + carrito + pago). La web cierra la venta.
- **Público principal:** adultos mayores y geriátricos / casas de cuidado de adultos. **Sub-público:** bebés.
- **Qué más valora el cliente +40:** (1) Precio / que le rinda, (2) Comodidad / que se lo lleven a la casa, (3) Calidad del producto.
- **Sensación al entrar:** cercana y de confianza (el negocio de barrio de toda la vida, pero online).

> Lectura de diseño: web de venta online, cálida y confiable, con foco en el cuidado del adulto mayor (dignidad + aliviar al cuidador), precio de fábrica y envío a domicilio bien visibles. Bebés como línea secundaria.

### Ronda 2 — El cliente que cuida a un adulto mayor
- **Mensaje que más pega:** Calidad que no falla (absorbe toda la noche sin pérdidas, producto propio de fábrica).
- **Dónde compra hoy y qué le molesta:** farmacia (caro) · tiene que ir a buscarlo (incómodo) · no sabe dónde comprar bien.
- **Frecuencia:** todos los meses → recompra/suscripción con recordatorio (aprovechar el cron que ya existe).
- **Factor decisivo para elegir la web:** (1) le llega a la casa (envío a domicilio), (2) asesoramiento de talle.

> Lectura de diseño: hero que combine **calidad que no falla** + **te llega a casa** + **precio de fábrica**. Ofrecer **asesoramiento de talle** (ayuda para elegir) y **recompra mensual**. Atacar el dolor "caro / incómodo / no sé dónde".

### Ronda 3 — Identidad de marca
- **Personalidad:** el experto que te cuida (sabe de pañales, asesora con seguridad, da tranquilidad).
- **Promesa / sello:** "Calidad de fábrica, precio justo".
- **Evitar:** que parezca barata / trucha (nada de look "oferta trucha", cuidar la confianza).
- **Nombre en la web:** Pañalera Ruta 8.

> Lectura de diseño: autoridad tranquila y confiable (experto que cuida), estética que transmita **calidad seria** (no barata). Reforzar "fábrica" como respaldo de calidad, no como "lo más barato".

### Ronda 4 — Estética visual
- **Paleta:** azul confianza + blanco (salud, higiene, confianza; serio y limpio). Acento a criterio.
- **Estilo:** limpio y claro tipo salud — mucho aire, **letra grande**, ordenado, fácil de leer (clave para +40).
- **Imágenes disponibles:** fotos reales de producto + logo. (Fábrica y demás, a futuro.)
- **Referencia:** a criterio profesional, priorizando la experiencia de +40.

> Lectura de diseño: paleta azul + blanco con un acento de salud (verde/celeste suave). Layout aireado, tipografía grande, alto contraste, componentes simples y grandes. Fotos reales de producto como protagonistas.

### Ronda 5 — Estructura de la web
- **Secciones sí o sí:** Catálogo/tienda + Asesor de talle/ayuda. (Sumar como apoyo: "cómo comprar/envíos" y "somos fábrica" para reforzar confianza.)
- **Primera pantalla (hero):** envío a domicilio bien visible + la promesa ("Calidad de fábrica, precio justo") + botón grande de comprar.
- **Navegación:** UNA sola página larga con scroll (más simple para +40, no se pierden).
- **Acciones secundarias:** pedir por WhatsApp + pedir asesoramiento de talle.

> Lectura de diseño: one-page scroll. Orden sugerido: Hero (promesa + envío + CTA comprar) → Catálogo → Asesor de talle → Cómo comprar/envíos → Somos fábrica (confianza) → Contacto. WhatsApp flotante fijo siempre visible.

### Ronda 6 — Hero y catálogo
- **Título hero:** generar 2-3 variantes para elegir (base: fábrica + envío + calidad/precio).
- **Precios en el catálogo:** precio visible + **descuento por cantidad** (bolsón: baja al llevar más).
- **Orden del catálogo:** a criterio → **Adulto primero** (público principal) con selector "¿Para quién? Adulto | Bebé".
- **Asesor de talle:** ⭐ **con IA de Claude** — un asesor inteligente en la web que responde y recomienda el talle/producto. (Se integra vía Edge Function para no exponer la API key; misma lógica que el bot.)

> Lectura de diseño: catálogo con precio + escalón por cantidad. Asesor de talle = mini-chat con IA (Claude) que pregunta y recomienda, con respaldo de WhatsApp. Hero con variantes de título.

### Ronda 7 — UX de compra / checkout
- **Registro:** compra directa (sin cuenta), con opción de guardar datos para la próxima.
- **Datos del pedido:** nombre + teléfono + dirección de entrega + **email** (el pedido se hace desde la web).
- **Carrito:** clásico, con página de carrito aparte.
- **Pago:** **Mercado Pago Checkout (pago en la web, API)** + transferencia + efectivo al recibir. (El webhook de MP ya está desplegado para confirmar el pago.)

> Lectura de diseño: catálogo → carrito (página) → checkout con datos mínimos → elegir forma de pago (MP Checkout online / transferencia / efectivo contra entrega). Pedido cae en el sistema (canal='web') y el pago MP se confirma solo.

### Ronda 8 — Accesibilidad y UX +40
- **Legibilidad:** NO se puede detectar la edad del visitante de forma confiable → se diseña **+40-friendly por defecto** (letra grande, alto contraste, botones grandes) + botón **A+ / A−** para ajustar el tamaño.
- **Dispositivo:** **celu primero** + responsive (breakpoints) para que en PC ande igual de bien.
- **Ayuda flotante:** el botón flotante siempre visible **ES el chatbot de la web** (asistente con IA) — une ayuda + asesor de talle + chat en uno.
- **Tono de textos:** mezcla (simple + cálido + práctico según la sección).

> Lectura de diseño: accesibilidad como prioridad (WCAG-friendly), toggle de tamaño de letra, mobile-first. El asistente IA flotante es el eje de ayuda (no un WhatsApp suelto).

### Ronda 9 — Asistente con IA de la web
- **Motor:** LLM con **prompt + contexto propio (OpenAI)**, integrado vía función segura (no exponer la API key).
- **Se presenta como:** asistente con nombre → **"Rita"**, cálida. Honesta: si preguntan, es la asistente (no miente que es humana).
- **Aparición:** botón flotante con cartel **"Hablá con un vendedor"** en loop de atención (aparece ~10 s, se esconde ~3-4 s, vuelve a salir). Nota de diseño: al abrirlo, Rita se presenta como asistente (cartel = gancho, adentro = honesto).
- **Integración:** silenciosa (no hace falta que se note) — el pedido web cae en el mismo sistema (canal='web').

> Lectura de diseño: widget de chat IA "Rita" flotante con animación peek-a-boo. Funciones a definir en su prompt (asesor de talle, precios del catálogo real, guiar la compra, derivar a humano). Backend: Edge Function que habla con el LLM + lee catálogo.

### Ronda 10 — Envío y logística
- **Zona de cobertura:** San Martín y alrededores (zona norte GBA).
- **Costo de envío:** GRATIS desde cierto monto (definir el monto). Empuja el ticket.
- **Tiempos:** dependen de la zona (mostrar "te avisamos según tu zona").
- **Retiro:** SÍ, retiro gratis en el local (opción en el checkout).

> Lectura de diseño: en el hero y el checkout, destacar "Envío GRATIS desde $__ en zona norte" + "o retiralo gratis en el local". Mostrar la zona con claridad.

> **★ REQUISITO (Rita editable):** el **system prompt de Rita** (comportamiento del asistente web) debe ser **100% editable desde el dashboard**, en la sección **"Chatbot Web"** que ya existe (hoy es solo tablero). Mismo patrón que el vendedor B2B (`b2b_config`): una tabla `web_config` (nombre asistente + system_prompt + activo), editor con textarea + Guardar en el panel, y Rita lee esa config. Yo redacto un prompt base; el dueño lo ajusta sin tocar código.

### Ronda 11 — Confianza y datos
- **Pruebas de confianza:** años / trayectoria + "somos fábrica" (dado). Reforzar el respaldo.
- **Reseñas:** todavía no hay → dejar la **sección lista, sin inventar** ninguna; se cargan después.
- **Garantía:** a criterio → **cambio de talle si no va** (bajo riesgo, seguro de cumplir, baja el miedo a comprar online).
- **Redes:** Instagram + Facebook + WhatsApp (pedir los links reales al construir).

> Lectura de diseño: bloque "Somos fábrica" + "X años" (dato a confirmar). Sección de reseñas maquetada pero vacía (placeholder honesto). Garantía de cambio de talle visible cerca del checkout. Íconos IG/FB/WhatsApp en el pie.

### Ronda 12 — Después de comprar
- **Post-compra:** confirmación clara + **resumen del pedido** (productos, total, entrega) + número de pedido + WhatsApp a mano.
- **Seguimiento:** SÍ, por WhatsApp (recibido / pago acreditado / en camino / entregado) — aprovecha el bot y el webhook ya armados.
- **Recompra:** las dos → botón **"volver a pedir lo de siempre"** (1 toque) + opción de **suscripción mensual**.
- **Sin stock:** mostrar en gris + **"avisame cuando llegue"** (deja contacto, se avisa al reponer).

> Lectura de diseño: pantalla de éxito con resumen + nº pedido. Avisos automáticos por WhatsApp (bot_outbox). Para el que vuelve: "repetir último pedido" destacado. Producto agotado = gris + captura de contacto para reposición.

### Ronda 13 — Cómo te encuentran / SEO
- **Fuentes de tráfico:** Google (búsqueda local) + redes (IG/FB) + boca a boca/volantes.
- **Búsquedas a ganar (SEO):** "pañales de adulto + zona norte / San Martín", "pañales con envío a domicilio", "pañales de bebé + zona".
- **Google Business:** no tiene, quiere → anotar como próximo paso (módulo 9).
- **Dominio:** **panaleraruta8.com.ar** (dominio objetivo).

> Lectura de diseño: SEO on-page para las búsquedas locales (títulos, meta, schema LocalBusiness), dominio claro y dictable. Preparar para linkear Google Business cuando exista.

### Ronda 14 — Scroll y movimiento (UX)
- **Estilo de scroll:** elegante y **sutil** — secciones que aparecen con fundido/subida suave al bajar (premium sin marear). Respetar `prefers-reduced-motion`.
- **Elementos fijos (sticky):** botón **Comprar/carrito** siempre a la vista + **Rita** flotante. (Sin sobrecargar: solo esos dos.)
- **Hero:** aparece suave al cargar (fade-in del título + botón).
- **Movimiento del scroll:** **scroll normal del celular** (NADA de smooth-scroll con inercia ni snap) — familiar y sin confundir a +40.

> Lectura de diseño: reveals `IntersectionObserver` fade-in-up sutiles, sin librería de smooth-scroll (scroll nativo). Sticky: carrito + Rita. Animaciones cortas y suaves, desactivables por reduce-motion. Nada mareador.

### Ronda 15 — Alcance y prioridades
- **v1:** la **web completa diseñada y navegable** (hero, catálogo, asesor Rita, confianza, contacto) — el checkout real con Mercado Pago se conecta como paso 2.
- **Productos:** de **demo** realistas ahora (se reemplazan por los reales / se conectan al catálogo del sistema después).
- **Imprescindible sí o sí:** que se vea **seria/confiable** + **Rita** (asistente IA) andando.
- **Deal-breakers (evitar):** que parezca **plantilla/genérica**, emojis/infantil de más, y que sea complicada.

---

## 🧭 NORTE CREATIVO (síntesis para construir)
- **Qué es:** tienda online one-page de una FÁBRICA de pañales, para vender directo a domicilio en zona norte GBA.
- **Público:** +40 que cuida a un adulto mayor (principal) y familias con bebés (secundario).
- **Promesa:** "Calidad de fábrica, precio justo" · envío a casa · asesoramiento.
- **Personalidad:** el experto que te cuida — cercano, confiable, honesto. NADA trucho ni genérico.
- **Estética:** azul confianza + blanco, tipo salud; limpio, aireado, **letra grande**, alto contraste, +40-friendly (toggle A+/A−). Fotos reales de producto. Sin emojis en la UI, sin look infantil.
- **Estructura (scroll):** Hero (promesa + envío gratis + CTA comprar) → Beneficios (fábrica / envío / calidad) → Catálogo (adulto primero, selector Adulto|Bebé, precio + escalón por cantidad) → Asesor de talle (Rita) → Cómo comprar / envío → Somos fábrica (confianza + trayectoria) → Reseñas (placeholder honesto) → Footer (IG/FB/WhatsApp, dominio panaleraruta8.com.ar).
- **UX:** mobile-first + responsive; scroll nativo con reveals sutiles (fade-in-up), sin smooth-scroll/snap, respeta reduce-motion. Sticky: carrito + Rita. Compra sin cuenta (datos: nombre, tel, dirección, email). Carrito clásico (página). Pago: MP Checkout + transferencia + efectivo al recibir. Post-compra: confirmación + resumen + nº + avisos WhatsApp. Recompra: "repetir lo de siempre" + suscripción. Sin stock: gris + "avisame".
- **Rita (asistente IA):** widget flotante con cartel "Hablá con un vendedor" en loop de atención (aparece 10s / se esconde 3-4s / vuelve); al abrir se presenta honesta como asistente. Motor LLM (OpenAI) con prompt + contexto vía Edge Function (no exponer key). **★ Su prompt es EDITABLE desde el dashboard → sección "Chatbot Web" (patrón `web_config`, como el B2B).** Funciones: asesor de talle, precios del catálogo real, guiar la compra, derivar a humano.
- **Backend / integración:** silenciosa. El pedido web cae en el mismo sistema (clientes/pedidos/pagos, canal='web'); MP webhook ya confirma pagos; avisos por bot_outbox. Catálogo público (anon lee activos) como se hizo con promociones.
- **SEO:** local para "pañales de adulto / bebé + zona norte / San Martín" y "envío a domicilio". Schema LocalBusiness. Dominio panaleraruta8.com.ar (arranca en Vercel).
- **Hosting:** Vercel (como lca-automatic).

## Pendiente de datos reales del dueño (para la versión final)
- Logo · fotos reales de producto · nº de WhatsApp oficial · dirección del local · años de trayectoria · monto de "envío gratis desde $__" · links de Instagram/Facebook · catálogo real con precios.

