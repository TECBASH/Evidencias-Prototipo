# Distribuidora Río Claro - Solución de IA con Microsoft Azure

**Enlace del prototipo funcional:**  
[Visitar Prototipo Funcional](https://rioclaro-ai-bash-cvdqb0a5dthbb3ct.westus3-01.azurewebsites.net)


---

## 1. Problema Resuelto
Distribuidora Río Claro contaba con 22 años de información fragmentada entre 5 sucursales, con catálogos duplicados en hojas de Excel y un proceso manual en cuentas por pagar que consumía 12 horas semanales a Laura, provocando pagos dobles de facturas y pérdidas de clientes por falta de respuesta oportuna.

Nuestra solución consolida:
1. **Extracción y Validación de Facturas (Laura):** Utiliza Azure AI Document Intelligence para extraer proveedor, fecha y total. Incorpora una regla de control que detecta folios ya procesados para evitar dobles pagos y marca para revisión humana facturas con confianza menor al 80%.
2. **Asistente Central Unificado (Clientes, Mariana y Toño):** Desplegado con Azure OpenAI (`gpt-4.1-mini`), unificando el catálogo de productos variados bajo una sola clave y ofreciendo existencias reales por sucursal y políticas oficiales. Incluye soporte de entrada y salida por voz optimizado para celular para el personal de bodega.

---

## 2. Principios de IA Responsable Aplicados

| Principio | Aplicación en el Prototipo |
| :--- | :--- |
| **Equidad** | La base de conocimiento consolida los datos de las 5 sucursales por igual, evitando que una sucursal con mayor volumen reciba atención preferencial. |
| **Confiabilidad y Seguridad** | Facturas con baja nitidez (<80% de confianza) o con datos duplicados no se pagan automáticamente; el sistema las envía a revisión manual. |
| **Privacidad y Seguridad** | No se enviaron nóminas ni contraseñas al modelo; los datos sensibles permanecen aislados de las consultas abiertas. |
| **Inclusión** | Interfaz adaptada con dictado y lectura de voz (Speech) utilizable desde el teléfono móvil para el personal que no opera computadoras. |
| **Transparencia** | El sistema declara ser un asistente de IA y cita las políticas oficiales de la empresa. |
| **Rendición de Cuentas** | La decisión final de pago permanece bajo autorización humana; la IA actúa como apoyo de extracción. |

---

## 3. Evidencias del Prototipo en Funcionamiento

### Interfaz del Asistente de IA (Chat de Existencias)
![Chat respondiendo existencias](https://i.postimg.cc/Y9GLfpKq/Chat.jpg)


### Alerta de Factura Duplicada (Azure AI Document Intelligence)
![Alerta de factura duplicada](https://i.postimg.cc/4d7HbJkJ/Facturas.jpg)
