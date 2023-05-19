- [Far2l репозиторий](https://github.com/elfmz/far2l)

Инструкция по установке

- Clone `git clone https://github.com/elfmz/far2l`


- Prepare build directory: 

`mkdir -p far2l/_build`

`cd far2l/_build`

- Build: with make:

`cmake -DUSEWX=yes -DCMAKE_BUILD_TYPE=Release ..`

`cmake --build . -j$(nproc --all)` 

`sudo make install`

`sudo ldconfig`