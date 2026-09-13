# Метадата
В первую очередь плагин должен содержать метаданные.
Метаданные хранятся в файле скрипта в формате комментариев. Должно быть окружено тегом METADATA с обоих сторон.
```
-- METADATA
...
-- METADATA
```

## Теги
&ast; - обязательные

- `METADATA`&ast; - начало/конец блока тегов
- `NAME <str>`&ast; - название плагина
- `DESCRIPTION <str>` / `DESC <str>` - описание плагина.
Если указать несколько раз, описание будет разделено на строки
- `AUTHOR <str>` - автор
- `VERSION <str>` - версия
- `REQUIRE <str...>` - используемые модули (для `require(m)`). Может быть указан несколько раз как `DESCRIPTION`

## Пример метаданных
```
-- METADATA
-- NAME Name of your plugin
-- DESCRIPTION Description
-- DESC Another line of description
-- AUTHOR You
-- VERSION 1.0.0
-- REQUIRE nyax.utils nyax.ui.builder
-- METADATA
```

Имея метаданные плагин уже может быть импортирован, даже если он не имеет никаких функций.