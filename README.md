# mdbook-sxi
Aquesta serà el respositori inicial amb les instruccions per crear la documentació del modul de Serveis de Xarxes i Internet.
**mdBook** és una eina per crear llibres, manuals i apunts a partir de fitxers **Markdown**.

## mdBook
- Creat inicialment per a la documentació de **Rust**.
- Permet escriure un llibre amb Markdown i exportar-lo com a web navegable.
- Característiques:
  - Genera índex i navegació automàtica.
  - Suporta cerca integrada.
  - Suporta temes i estils personalitzats.
  - Es pot desplegar fàcilment amb GitHub Pages.

## Instruccions
En aquestes instruccions es descriuran les passes per instal·lar mdBook, crear un mdBook, publicar-lo amb GitHub Pages.
1. Assegura't de tenir instal·lat **Rust**: [Instal·lació](https://www.rust-lang.org/tools/install).
2. Executa la següent ordre per instal·lar mdBook:
   ```bash
   cargo install mdbook
   ```
3. Clona el repositori a l'ordinador.
   - Ves a la pàgina del teu repositori dins l'organització [if31cSXI](https://github.com/ifc31cSXI).
   - Copia l'adreça HTTPS del botó verd "Code".
   - Obre el terminal i executa:
   ```bash
   git clone https://github.com/ifc31cSXI/nom-del-teu-repositori.git
   cd nom-del-teu-repositori
   ```
4. Crear un directori a on es trobará la documentació.
   ```bash
   mkdir mdbooksxi
   cd mdbooksxi
   ```
5. Crear l'estructura bàsica de mdbook.
   ```bash
   mdbook init
   ```
   - `book.toml`: configuració del llibre.
   - `src/SUMMARY.md`: índex de continguts.
   - `src/*.md`: capítols en Markdown. -
6. Dins `src/SUMMARY.md` crear l'estructura de continguts del llibre per exemple:
   ```
   - [Chapter 1](./chapter_1.md)
   - [Chapter 2](./chapter_2.md)
   - [Chapter 3](./chapter_3.md)
   ```
7. Dins els fitxers `chapter_1.md`, `chapter_2.md` ... S'ha de fe la documentació de cada apartat.
8. Generar i veure el llibre.
   ```bash
   mdbook build   # genera el llibre a /book
   mdbook serve   # inicia un servidor local (http://localhost:3000)
   ```
9. Comprovar el contingu del llibre.
10. Fer un commit i push.
11. Anar els `Settings` del repositori i desprès a `pages`.
12. Anar a `Source` i seleccionsr `GitHub Actions`.
13. Seleccionar `mdbook` i pitjar `configure`
14. Pijar a `Commit changes`. Això crea el `mdbook.yml` dins el directori `workflows` per generar el workflow actions.
15. Comprovar que el github pages s'ha publicat `https://josemmol.github.io/nom del teu repositori`.
## Lliurament
Només cal fer commits i push al teu repositori generat per GitHub Classroom.
