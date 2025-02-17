# 🖥️🔧 Personalización del Display ST7920 en Ender 3 con Klipper

Este repositorio proporciona archivos de configuración (`.cfg`) para personalizar la pantalla LCD **ST7920** original de la **Ender 3** con **Klipper**. Gracias a estos ajustes, el display monocromático podrá:

✅ **Mostrar datos en tiempo real** de la impresión.  
✅ **Traducir el menú al español** para una mejor experiencia.  
✅ **Personalizar completamente** su contenido y apariencia.  
✅ **Incluir un splash screen editable** con la imagen de inicio que prefieras.  

---

## 📌 Verifica la compatibilidad  

Antes de comenzar, asegúrate de que tu pantalla es compatible. Debes agregar las siguientes líneas a tu `printer.cfg` si aún no están incluidas:

```ini
[display]
lcd_type: st7920                       # Tipo de pantalla LCD utilizado
cs_pin: EXP1_7                         # Pin de selección de chip (CS) para la pantalla
sclk_pin: EXP1_6                        # Pin de reloj (SCLK) para la pantalla
sid_pin: EXP1_8                        # Pin de datos en serie (SID) para la pantalla
encoder_pins: ^EXP1_5, ^EXP1_3         # Pines del codificador rotativo para el control del menú
click_pin: ^!EXP1_2                    # Pin de clic para el codificador (botón)
