# 🛠️ MinGW-w64 - Minimalist GNU for Windows

## 📝 Descripción

MinGW-w64 es un fork avanzado del proyecto MinGW original que proporciona un entorno de desarrollo completo para crear aplicaciones nativas de Windows utilizando herramientas GNU. Este proyecto incluye compiladores GCC para arquitecturas de 32 y 64 bits, bibliotecas de tiempo de ejecución C, headers de Windows API y herramientas de desarrollo esenciales.

## ✨ Características principales

- 🎯 **Soporte completo para 64-bit y 32-bit**: Compiladores GCC nativos para ambas arquitecturas
- 🔧 **Headers completos de Windows API**: Conjunto extenso de headers para desarrollo en Windows
- 📚 **Bibliotecas de runtime C/C++**: CRT (C Runtime) completamente funcional
- 🔄 **Cross-compilation**: Capacidad de compilación cruzada desde múltiples plataformas
- 🛡️ **Compatibilidad POSIX**: Herramientas y utilidades compatibles con estándares POSIX
- 📦 **Autotools**: Sistema de construcción basado en autoconf/automake
- 🎛️ **Configuración flexible**: Múltiples opciones de configuración para diferentes casos de uso

## 🖼️ Capturas de pantalla

```bash
# Ejemplo de configuración del proyecto
./configure --with-headers --with-crt --with-libraries=all --with-tools=all

# Compilación exitosa
make && make install
```

## 🔧 Tecnologías utilizadas

- ![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white) **Lenguaje C**: Core del runtime y headers
- ![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white) **C++**: Bibliotecas de soporte C++
- ![Assembly](https://img.shields.io/badge/Assembly-654FF0?style=flat&logo=assemblyscript&logoColor=white) **Assembly**: Optimizaciones de bajo nivel
- ![GNU](https://img.shields.io/badge/GNU-A42E2B?style=flat&logo=gnu&logoColor=white) **GNU Autotools**: Sistema de construcción
- ![Shell](https://img.shields.io/badge/Shell_Script-121011?style=flat&logo=gnu-bash&logoColor=white) **Shell Scripts**: Scripts de configuración y construcción

## 📥 Instalación y uso

### ⚡ Instalación rápida

```bash
# Clonar el repositorio
git clone https://github.com/mingw-w64/mingw-w64.git
cd mingw-w64

# Configuración básica
./configure --with-headers --with-crt

# Compilación e instalación
make && sudo make install
```

### 🔧 Configuración avanzada

```bash
# Configuración completa con todas las características
./configure \
  --with-headers \
  --with-crt \
  --with-libraries=all \
  --with-tools=all \
  --prefix=/opt/mingw-w64

# Para desarrollo con bibliotecas específicas
./configure \
  --with-headers \
  --with-crt \
  --with-libraries=libmangle,pseh \
  --with-tools=gendef,genidl
```

### 🎯 Opciones de configuración

| Opción | Descripción |
|--------|-------------|
| `--with-headers` | 📁 Instala los headers de Windows API |
| `--with-crt` | 🔧 Construye el C Runtime |
| `--with-libraries=all` | 📚 Construye todas las bibliotecas opcionales |
| `--with-tools=all` | 🛠️ Construye todas las herramientas adicionales |

## 📁 Estructura del proyecto

```
mingw-w64/
├── 📄 AUTHORS                           # Lista de contribuidores
├── 📄 COPYING                          # Información de licencia
├── 📄 DISCLAIMER                       # Descargo de responsabilidad
├── ⚙️ configure                        # Script de configuración principal
├── 📝 configure.ac                     # Configuración de autoconf
├── 📋 Makefile.am                      # Plantilla de Makefile
├── 🔧 build-aux/                       # Herramientas de construcción
│   ├── config.guess                    # Detección de plataforma
│   ├── config.sub                      # Validación de configuración
│   ├── install-sh                      # Script de instalación
│   └── missing                         # Manejo de herramientas faltantes
├── 📁 mingw-w64-headers/               # Headers de Windows API
├── 📁 mingw-w64-crt/                   # C Runtime libraries
├── 📁 mingw-w64-libraries/             # Bibliotecas adicionales
│   ├── libmangle/                      # Biblioteca de name mangling
│   └── pseh/                           # Manejo de excepciones SEH
├── 📁 mingw-w64-tools/                 # Herramientas de desarrollo
│   ├── gendef/                         # Generador de archivos .def
│   └── genidl/                         # Generador de archivos IDL
└── 📁 mingw-w64-doc/                   # Documentación
    ├── headers-ref/                     # Referencia de headers
    └── howto-build/                     # Guías de construcción
```

### 🧩 Componentes principales

- **Headers**: 📂 Conjunto completo de headers de Windows API
- **CRT**: 🏗️ C Runtime Library para aplicaciones Windows
- **Libraries**: 📚 Bibliotecas adicionales como libmangle y pseh
- **Tools**: 🔨 Herramientas como gendef y genidl

## 👥 Autores / Colaboradores

### 🚀 Maintainers principales
- **Mook** - 📧 mook.gcc@gmail.com
- **NightStrike** - 📧 nightstrike@gmail.com  
- **Kai Tietz** - 📧 kai.tietz@redhat.com

### 🤝 Desarrolladores con acceso de escritura
- **kjk_hyperion** - ReactOS contributor
- **Tor Lillqvist** - 📧 tlillqvist@gmail.com
- **Alexey Pushkin** - 📧 Alexey.Pushkin@mererand.com
- **Roland Schwingel** - OneVision Software AG
- **Ozkan Sezer** - 📧 sezeroz@gmail.com
- **Chris Sutcliffe** - 📧 ir0nh34d@gmail.com
- **Jonathan Yong** - 📧 jon_y@users.sourceforge.net

### 🙏 Agradecimientos especiales
- **ReactOS Project** - 🌟 Contribuciones fundamentales
- **Wine Project** - 🍷 Headers y IDL files
- **OneVision Software AG** - 🏢 Soporte corporativo

## 📜 Licencia

Este proyecto está licenciado bajo múltiples licencias:

- 🔓 **Zope Public License (ZPL) Version 2.1** - Componentes principales
- 🆓 **Public Domain** - Algunos archivos específicos  
- 📋 **LGPL** - Headers y IDL importados de Wine
- 🛡️ **BSD/MIT** - Componentes específicos como getopt

Ver los archivos `COPYING*` para detalles completos de licenciamiento.

## 🤝 Contacto para empresas / Colaboraciones

### 📧 Contactos oficiales
- **Lista de correo principal**: mingw-w64-public@lists.sourceforge.net
- **Reportes de bugs**: [Tracker en SourceForge](http://sourceforge.net/projects/mingw-w64/)
- **Sitio web oficial**: [mingw-w64.org](http://mingw-w64.org/)

### 🏢 Para colaboraciones empresariales
- Soporte comercial disponible a través de la comunidad
- Contribuciones corporativas bienvenidas
- Consultas sobre licenciamiento: contactar a los maintainers principales

### 🌐 Recursos adicionales
- 📖 **Documentación**: Ver directorio `mingw-w64-doc/`
- 🔧 **Guías de construcción**: `howto-build/mingw-w64-howto-build.txt`
- 📚 **Referencia de headers**: `headers-ref/header_doc.txt`

---

<div align="center">

**⭐ Si este proyecto te ha sido útil, ¡no olvides darle una estrella! ⭐**

[![GitHub stars](https://img.shields.io/github/stars/mingw-w64/mingw-w64?style=social)](https://github.com/mingw-w64/mingw-w64/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/mingw-w64/mingw-w64?style=social)](https://github.com/mingw-w64/mingw-w64/network/members)

</div>
