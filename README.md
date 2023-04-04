# Подключение SFML к Windows проекту через CMake

## Необходимые инструменты:

* [MSYS2](msys2.org)

## В данном проекте мы будем пользовать средой MinGW64 от MSYS2

### Последовательность действий:

Установка [MSYS2](msys2.org) по стандартному пути С:\msys64

Открываем оболочку MinGW64 в пути C:\msys64\mingw64

Устанавливаем стандартные средства разработки (с компилятором и сборщиком) через пакетный менеджер pacman в данной оболочке
```bash
User@PC MINGW64 ~
$ pacman -S mingw-w64-x86_64-toolchain
```

Устанавливаем здесь же сборщик проектов CMake
```bash
User@PC MINGW64 ~
$ pacman -S mingw-w64-x86_64-cmake
```

Устанавливаем библиотеку SFML
```bash
User@PC MINGW64 ~
$ pacman -S mingw-w64-x86_64-sfml
```

Собираем конфигурацию проекта через CMake нашего проекта в директорию build
```bash
User@PC MINGW64 /path-to-project/TestSFML/build
$ cmake -G "MinGW Makefiles" ..
```

Собираем исполняемые файлы из полученных ранее конфигурационных файлов в директории build
```bash
User@PC MINGW64 /path-to-project/TestSFML/build
$ cmake --build .
```

Теперь в директории /path-to-project/TestSFML/build будут находиться необходимые нам бинарные\исполняемые файлы
