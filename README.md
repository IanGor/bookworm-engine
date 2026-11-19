# BookwormEngine

Общий Rust-движок Android- и Linux-читалок Bookworm: разбор FB2, FB2.ZIP и EPUB, типографика, переносы, вёрстка и отрисовка страниц. `crates/bw-render` — эталонный вывод PNG для проверок вёрстки. Первоначальный код перенесён из BookWorm (коммит `65517491113e28d493a658d917d449e0d632b323`) без изменения алгоритмов.

При локальной разработке этот репозиторий лежит рядом с `Bookworm` и `BookwormCLI`. Оба приложения собираются с одним `crates/core`; после изменений ядра пересоберите нужное приложение.

```sh
cargo test --workspace --locked
cargo run --release --locked -p bw-render -- tests/corpus/synthetic/02_structure_ru.fb2 --family 'PT Serif' --mono fonts/LiberationMono-Regular.ttf --pages 1-3
```

В `fonts/` лежат общие гарнитуры, в `tests/` — только тестовые данные. См. `LICENSE` и `NOTICE`.
