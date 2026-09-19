# 🚀 Preservando SSDs en Tiempos de Crisis: El Experimento del Over-Provisioning (OP)

> **¿Es el Over-Provisioning la clave para salvar las unidades de almacenamiento económicas frente a la escasez de componentes?**

Bienvenido a este repositorio de investigación empírica. Aquí analizamos y documentamos los resultados de una **prueba de estrés continua** aplicada a SSDs de gama baja, con el objetivo de demostrar si aplicar **Over-Provisioning (OP)** es una práctica indispensable para preservar la vida útil de las unidades de estado sólido y mantener su rendimiento constante.

---

## 💥 El Origen: La Crisis de Componentes (2025 - 2026)

Con la crisis global de componentes derivada del auge de la **Inteligencia Artificial (2025–2026)**, encontrar almacenamiento económico y confiable se ha vuelto una misión casi imposible. 

El mercado se ha inundado de SSDs de gama baja o de marca blanca. La mayoría de estas unidades presentan severas deficiencias:
* ⚠️ **Controladoras limitadas** sin optimizaciones avanzadas.
* ⚠️ **Firmwares básicos** que no gestionan eficientemente el desgaste.
* ⚠️ **Memorias NAND de menor durabilidad**, vulnerables al desgaste acelerado.

Esta combinación pone en riesgo directo nuestros datos, acelerando la muerte prematura de las unidades. Para colmo, ante la falta de stock, [algunos fabricantes han comenzado a negar sustituciones y ofrecer únicamente reembolsos](https://revistacloud.com/la-escasez-de-ssd-llega-a-las-garantias-sk-hynix-ofrece-reembolsos-ante-la-falta-de-stock/). 

📌 **Nuestra misión:** Buscar formas prácticas de extender la durabilidad y consistencia del almacenamiento existente, priorizando la **confiabilidad de los datos** por encima del espacio bruto.

---

## 🧪 La Prueba: Enfrentamiento Directo

Para evaluar el impacto real del **Over-Provisioning**, hemos sometido a pruebas extremas dos unidades idénticas en marca, modelo y capacidad base, diferenciándolas únicamente por la asignación de espacio sin formatear:

| Característica | 🔵 Competidor 1 | 🔴 Competidor 2 |
| :--- | :--- | :--- |
| **Modelo** | KingSpec P4 120 GB | KingSpec P4 120 GB |
| **Fabricante de Controladora** | Maxio | Realtek |
| **Modelo de Controladora** | MAS1102B-B1C | Raymx 1135T |
| **Tipo de Memoria NAND** | TLC Hynix 3Dv6 | TLC Hynix 3Dv6 |
| **Over-Provisioning (OP)** | **25% Asignado** ⚙️ | **0% (Capacidad Total)** ❌ |

> 💡 **¿Por qué esta prueba?** Al dejar un 25% de espacio sin asignar, se le otorga a la controladora un "margen de maniobra" exclusivo para ejecutar tareas pesadas de limpieza y nivelación sin saturar las celdas de memoria.

---

## 📂 Estructura del Repositorio y Avances

* 📄 **Carpeta Raíz (`/`)**: Documentación teórica, metodologías, explicaciones técnicas y análisis consolidados.
* 📊 **`/Historial clínico Maxio`**: Capturas de pantalla, datos numéricos y gráficas de rendimiento del **Competidor 1 (Con OP)**.
* 📊 **`/Historial clínico Realtek`**: Capturas de pantalla, datos numéricos y gráficas de rendimiento del **Competidor 2 (Sin OP)**.

---

## 📺 Cobertura en Video y Seguimiento en Vivo

Puedes seguir la evolución del experimento, los análisis en video y las pruebas en tiempo real a través de los siguientes enlaces:

* 🎥 **Canal de YouTube:** [@CaletayoAhata](https://youtube.com/@caletayoahata2584?si=yNBGVO2-CKoaAWhb)
* 🍿 **Lista de Reproducción:** [Serie de Pruebas de Estrés en SSDs](https://youtube.com/playlist?list=PLLap9Bu3fqzE&si=qboD7iRomu6aD2ZR)

---

## 📖 Glosario Técnico

 Para entender a fondo los datos y métricas reportados en las capturas, ten en cuenta los siguientes conceptos:

* 🛡️ **OP (Over-Provisioning / Sobredimensionamiento):** Reserva de un porcentaje de la capacidad bruta del SSD para uso exclusivo del controlador. Ayuda a la recolección de basura, nivelación de desgaste y reducción drástica del WAF.
* 📈 **WAF (Write Amplification Factor / Factor de Amplificación de Escritura):** Relación entre los datos que el sistema envía a escribir y los que físicamente se escriben en la NAND. *Un WAF alto degrada el disco rápidamente; el objetivo del OP es reducirlo.*
* 🧹 **Garbage Collection (GC / Recolección de Basura):** Proceso interno autónomo que identifica y libera bloques con páginas no válidas para dejarlos listos para nuevas escrituras.
* ✂️ **TRIM:** Comando del SO que notifica a la controladora qué bloques contienen datos borrados para que el Garbage Collection pueda procesarlos con anticipación.
* ⚖️ **Wear Leveling (Nivelación de Desgaste):** Algoritmo que distribuye escrituras y borrados de forma uniforme en todas las celdas para evitar el fallo prematuro de sectores específicos.
* 💾 **NAND Flash:** Chips de memoria no volátil donde se guardan los datos. Tienen un número finito de ciclos de escritura/borrado (P/E cycles).
* 🧱 **Bad Block Management:** Mecanismo interno que detecta y aisla las celdas defectuosas o que han llegado al final de su vida útil.

---

## 🎯 Conclusión Preliminar

> **El Over-Provisioning no es desperdiciar almacenamiento:** es regalarle una "segunda vida" a tu SSD. En épocas de precios inflados y escasez de componentes, aprender a optimizar nuestro hardware es la mejor herramienta para proteger nuestros datos y nuestra billetera.
