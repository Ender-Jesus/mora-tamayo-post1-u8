# lab8\_pos1

Laboratorio 8 Postcontenido 1

\# apellido-post1-u8 — Operaciones con Cadenas en NASM x86



\## Descripción

Laboratorio de instrucciones de procesamiento de cadenas en NASM bajo DOSBox:

REP MOVSB/W, REPNE SCASB y REPE CMPSB.



\---



\## Archivos

\- `post1.asm` — Copia de cadena con REP MOVSB y versión optimizada con REP MOVSW

\- `post1c.asm` — Búsqueda de carácter con REPNE SCASB

\- `post1d.asm` — Comparación de cadenas con REPE CMPSB



\---



\## Resultados por Checkpoint



\*\*Checkpoint 1 — REP MOVSB\*\*

Copia 13 bytes de `origen` ("HOLA, MUNDO!") a `destino`.

Salida: `Copiado: HOLA, MUNDO!`



\*\*Checkpoint 2 — REP MOVSW\*\*

Misma copia optimizada: 6 words (12 bytes) con MOVSW + 1 byte sobrante con MOVSB.

Salida idéntica: `Copiado: HOLA, MUNDO!`



\*\*Checkpoint 3 — REPNE SCASB\*\*

Búsqueda del carácter `'d'` en `"Arquitectura de Computadores"`.

Salida: `Hallado en posicion: 13`

Al buscar `'z'`: `No encontrado.`



\*\*Checkpoint 4 — REPE CMPSB\*\*

Comparación de `"NASM x86"` vs `"NASM x86"` → `Iguales.`

Comparación de `"NASM x86"` vs `"NASM ARM"` → `Diferentes.` (diverge en posición 5)



\---



\## Entorno

\- DOSBox 0.74

\- NASM (formato binario `-f bin`)

\- Compilación: `nasm -f bin archivo.asm -o archivo.com`

