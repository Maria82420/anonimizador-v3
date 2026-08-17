# Reglas y Arquitectura: Anonimizador Legal-Tech V3

## 🛡️ Propósito
Plataforma web autónoma de seudonimización y privacidad local en RAM (Ley Argentina 25.326 y RGPD) para ofuscar PII y datos sensibles en escritos judiciales, contratos, PDFs y DOCX antes de enviarlos a modelos de IA.

## ⚖️ Reglas de Oro de Privacidad y Cumplimiento
1. **Zero External Requests / Zero Leakage:** Todo el procesamiento ocurre 100% en la memoria RAM del navegador. Cero telemetría externa.
2. **Consentimiento Opt-In Estricto:** Cualquier casilla de verificación (*checkbox*) debe estar **DESMARCADA POR DEFECTO**.
3. **Ofuscación Robusta:** Soporte para reemplazo de variables procesales (`[ACTOR_1]`, `[DEMANDADO]`, `[DNI]`, `[JUZGADO]`, `[MONTO]`, `[DOMICILIO]`).
4. **Seguridad del DOM:** Manipulación segura mediante `textContent` (prevenir inyección DOM-XSS) y callbacks puros en reemplazos de expresiones regulares.

## 🧱 Estructura del Repositorio
- `index.html`: Aplicación web standalone V3 con dependencias modulares (Tailwind CSS, PDF.js, Mammoth.js).
- `anonimizador_offline.html`: Versión autoportante Búnker (librerías embebidas en base64 para uso 100% offline).
- `README.md`: Documentación y principios del proyecto.
