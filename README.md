#!/bin/bash
# 🖥️🔧 ¡Personaliza el Display ST7920 de tu Ender 3 con Klipper!

# Este script detalla cómo personalizar la pantalla LCD monocromática ST7920 en la Ender 3,
# mostrando datos en tiempo real, un menú en español y un splash screen personalizable.

echo "✅ Características:"
echo "- Visualización en tiempo real de los datos de impresión 📊"
echo "- Menú completo en español 🌍"
echo "- Personalización de la interfaz y el diseño 🔧"
echo "- Splash screen editable al encender 🚀"

# 📌 Paso 1: Verificar la compatibilidad
echo "🔍 Verificando compatibilidad del display ST7920..."
cat <<EOL >> printer.cfg
[display]
lcd_type: st7920                       # Tipo de pantalla LCD
cs_pin: EXP1_7                         # Pin de selección de chip (CS)
sclk_pin: EXP1_6                        # Pin de reloj (SCLK)
sid_pin: EXP1_8                        # Pin de datos en serie (SID)
encoder_pins: ^EXP1_5, ^EXP1_3         # Pines del codificador rotativo
click_pin: ^!EXP1_2                    # Pin del botón del codificador
EOL
echo "✅ Configuración de pantalla agregada a printer.cfg"

# 📂 Paso 2: Agregar los archivos de configuración
echo "📂 Incluyendo los archivos de personalización en printer.cfg..."
cat <<EOL >> printer.cfg
[include menu.cfg]          # Menú traducido al español
[include display.cfg]       # Configuración de visualización
[include custom_display.cfg] # Personalización avanzada del display
EOL
echo "✅ Archivos de configuración añadidos."

# 🛠 Paso 3: Personalización del menú y el splash screen
echo "🛠 Personalizando el menú y el splash screen..."
echo "- Los archivos menu.cfg, display.cfg y custom_display.cfg son totalmente editables."
echo "- Puedes personalizar textos, iconos y el splash screen a tu gusto."

# 📸 Opción avanzada: Editar Splash Screen
echo "📸 Para personalizar el splash screen, edita el archivo custom_display.cfg"
echo "   Aquí puedes modificar el diseño y los textos de bienvenida."

# 📌 Instalación rápida
echo "🚀 Instalación rápida:"
echo "1️⃣ Descarga los archivos .cfg del repositorio."
echo "2️⃣ Copia los archivos a la carpeta de configuración de tu impresora."
echo "3️⃣ Edita las opciones según tu impresora."
echo "4️⃣ Reinicia Klipper para aplicar los cambios."

# 📢 Conéctate conmigo
echo "📢 Conéctate conmigo:"
echo "🔗 TikTok: https://www.tiktok.com/@fuzion3d"
echo "📸 Instagram: https://www.instagram.com/fuzion3dcrea"
echo "🎥 YouTube: https://youtube.com/@fuzion3dcrea"
echo "💬 WhatsApp (Klipperianos): https://chat.whatsapp.com/IHaUnmBsNPnJ1kDIenCrmT"

# 🚀 Finalización
echo "🔥 ¡Disfruta de un display personalizado en tu Ender 3 con Klipper!"
