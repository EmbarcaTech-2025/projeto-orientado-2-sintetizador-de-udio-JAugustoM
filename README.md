
# Projetos de Sistemas Embarcados - EmbarcaTech 2025

Autor: **José Augusto Alves de Moraes**

Curso: Residência Tecnológica em Sistemas Embarcados

Instituição: EmbarcaTech - HBr

Brasília, Junho de 2025

---

## Objetivos

O objetivo deste projeto foi implementar um sintetizador de audio utilizando a BitDogLab.

---

## Componentes Utilizados

Para desenvolver o projeto foi utilizado os seguintes componentes da BitDogLab.

| Componente         | Quantidade | GPIO               |
| ------------------ | ---------- | -------------------|
| Botão              | 2          | 5, 6               |
| Buzzer             | 1          | 21                 |
| Display OLED       | 1          | 14 (SDA), 15 (SDC) |
| LED RGB            | 1          | 11 (G), 13 (R)     |
| Microfone          | 1          | 28                 |

---

## Utilização

### Dependêcias

- [Pico C SDK](https://github.com/raspberrypi/pico-sdk)
- [Picotool](https://github.com/raspberrypi/picotool)
- [Just](https://github.com/casey/just)

### Como Compilar e Executar

Para compilar o projeto é possível utilizar a extensão da Pico C SDK ou o terminal, executando o seguinte comando na raiz do projeto.

`cmake -S . -B build -G Ninja && ninja -C build`

Após compilar o projeto basta passar o arquivo para a placa com o comando a seguir:

`sudo picotool load build/src/app/sintetizador.elf`

Caso tenha o [just](https://github.com/casey/just) instalado é possível utilizar os dois comandas a seguir ao invés dos mencionados acima:

`just build`

`just load sintetizador`

---

## 📜 Licença

GNU GPL-3.0.
