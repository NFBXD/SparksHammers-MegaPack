# Spark's Hammers Mega Pack — исходный код / source code

Дополнение к **Spark's Hammers 1.7.10 (1.6.1)** автора Brightspark. Неофициальное, изменённая версия оригинала.
An unofficial addon / modified version of Spark's Hammers by Brightspark (Minecraft 1.7.10, Forge).

**Лицензия / License:** GNU General Public License v2 (текст в файле `LICENSE`), как и у оригинала.

## Что изменено / What was changed

Оригинальные классы и ресурсы мода не менялись, кроме языковых файлов. Добавлено:
- `src/` — исходники аддона (отдельный `@Mod`, модид `SparksHammers5x5`, зависит от `SparksHammers`):
  - `Hammer5x5Addon` — регистрация предметов и рецептов (молоты, экскаваторы, гибриды 5×5…17×17, инструменты из блоков, универсальные, бесконечные, бедроковые);
  - `ItemHammer5x5`, `ItemExcavatorSized`, `ItemHammerExcavator` — инструменты с настраиваемым радиусом;
  - `ItemUniversalHammer`, `ItemUniversalExcavator` — эффективны на любых блоках;
  - `ItemBedrockHammer`, `ItemBedrockExcavator`, `IBedrockBreaker`, `BedrockBreakHandler` — инструменты, ломающие бедрок;
- `assets/` — новые текстуры (`textures/items`) и дополненные `lang/en_US.lang`, `lang/ru_RU.lang` (русский перевод для новых предметов).
  Текстуры сделаны перекраской текстур оригинального мода и распространяются на тех же условиях.
- `stubs/` — заглушки классов Minecraft/Forge только для компиляции (в мод не попадают).

## Сборка / Build

Нужны JDK 8+, `unzip`, `zip` и оригинальный `SparksHammers-1.7.10-1.6.1.jar`:

    ./build.sh /путь/к/SparksHammers-1.7.10-1.6.1.jar

Результат: `build/SparksHammers-MegaPack.jar`. Оригинальный мод внутри него сохраняется, ставить рядом отдельно не нужно.

Приватное поле `mineRadius` у оригинальных `ItemHammer`/`ItemExcavator` задаётся через reflection, поэтому оригинальные классы менять не пришлось.
