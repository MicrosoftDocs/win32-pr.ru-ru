---
title: Структуры DirectWrite
description: DirectWrite определяет следующие структуры.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f678be8e02c8afecd849673d97ae20f6b1a710
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587914"
---
# <a name="directwrite-structures"></a>Структуры DirectWrite

DirectWrite определяет следующие структуры.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | Представляет данные точечного рисунка в формате BGRA32. |
| [**ДВРИТЕные \_ \_ метрики курсора**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | Структура [**\_ \_ метрик курсора дврите**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) задает метрики для размещения курсора в шрифте. |
| [**\_ \_ метрики кластера дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Содержит сведения о кластере глифов. |
| [**ДВРИТЕ \_ Color \_ F**](dwrite-color-f.md) | Описывает красный, зеленый, синий и альфа-компоненты цвета. |
| [**ДВРИТЕ \_ Цвет \_ глифа цвета \_**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Содержит сведения, необходимые модулям подготовки отчетов для отрисовки глифов с использованием сведений о цвете глифа. |
| [**\_Глиф цвета \_ дврите \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Представляет запуск глифа цвета. Метод IDWriteFactory4:: Транслатеколорглифрун возвращает упорядоченную коллекцию символов цветового глифа для различных типов в зависимости от того, что поддерживает шрифт. |
| [**\_фрагмент файла \_ дврите**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Представляет диапазон байтов в файле шрифта. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Представляет минимальный и максимальный диапазоны возможных значений для оси шрифта. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Представляет значение для оси шрифта. Используется при запросе и создании экземпляров шрифтов. |
| [**\_функция ШРИФТА \_ дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Указывает свойства, используемые для обозначения и выполнения типографских функций в текущем начертании шрифта. |
| [**\_ \_ метрики шрифта дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | Структура [**\_ \_ метрик шрифта дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) задает метрики, применимые ко всем глифам в гарнитуре шрифта. |
| [**ДВРИТЕ \_ Font \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | Структура [**\_ \_ METRICS1 Font дврите**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) определяет метрики, применимые ко всем глифам в гарнитуре шрифта. |
| [**\_свойство ШРИФТА \_ дврите**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Свойство Font, используемое для фильтрации наборов шрифтов и создания набора шрифтов с явными свойствами. |
| [**\_данные изображения глифа дврите \_ \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Данные для одного глифа из Жетглифимажедата. |
| [**\_метрики глифов дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Задает метрики отдельного глифа. |
| [**\_смещение глифа дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Необязательная коррекция для расположения глифа. |
| [**\_выполнение глифа дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Содержит сведения, необходимые для отрисовки выполнения глифов модулями подготовки отчетов. |
| [**\_Описание запуска глифа дврите \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Содержит дополнительные свойства, связанные с теми, которые [**выполняются в дврите \_ глифа \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**\_ \_ метрики проверки ПОПАДАНИя дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Описывает регион, полученный при проверке нажатия. |
| [**ДВРИТЕ \_ встроенные \_ \_ метрики объектов**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Содержит свойства, описывающие геометрическое измерение определяемого приложением встроенного объекта. |
| [**\_возможность обоснования дврите \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | Структура [**\_ \_ возможностей обоснования дврите**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) указывает сведения об обоснованиях на глиф. |
| [**\_ \_ точка останова дврите Line**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Характеристики точки останова в символе. |
| [**\_ \_ метрики линии дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Содержит сведения о форматированной строке текста. |
| [**ДВРИТЕ \_ Line \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Содержит сведения о форматированной строке текста. |
| [**ДВРИТЕ \_ \_ междустрочный**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**\_Матрица дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | Структура [**\_ матрицы дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) указывает преобразование графики, применяемое к визуализированным глифам. |
| [**\_метрики выступа дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Указывает, какой объем видимых DIP (аппаратно-независимых пикселей) отклонение с каждой стороны макета или встроенных объектов. |
| [**ДВРИТЕ \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | [**Дврите \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) Union описывает значения классификации гарнитуры, используемые с [**IDWriteFont1:: жетпаносе**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) для выбора и сопоставления шрифта. |
| [**\_анализ скриптов \_ дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Сохраняет связь текста и его системного сценария записи, а также некоторые атрибуты вывода. |
| [**\_Свойства сценария \_ дврите**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | Структура [**\_ \_ свойств скрипта дврите**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) задает свойства скрипта для навигации и обоснования курсора. |
| [**\_ \_ Свойства глифа формирования дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Содержит свойства выходных данных формирования для выходного глифа. |
| [**\_ \_ Свойства текста для формирования дврите \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Формирование выходных свойств для выходного глифа. |
| [**ДВРИТЕ \_ Зачеркнутый**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Содержит сведения о размере и размещении зачеркивания. |
| [**ДВРИТЕ \_ текстовые \_ метрики**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Содержит метрики, связанные с текстом после макета. |
| [**ДВРИТЕ \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Содержит метрики, связанные с текстом после макета. |
| [**\_диапазон текста \_ дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Задает диапазон позиций текста, в котором формат применяется в тексте, представленном объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . |
| [**ДВРИТЕ \_ Обрезка**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Задает параметр обрезки для текста, передающего поле макета.  |
| [**\_типографские \_ функции дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Содержит набор типографских функций, применяемых во время формирования текста. |
| [**подчеркивание ДВРИТЕ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Содержит сведения о ширине, толщине, смещении, высоте запуска, направлении чтения и направлении потока подчеркивания.  |
| [**ДВРИТЕ \_ \_ диапазон Юникода**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | Структура [**\_ \_ диапазона Юникода дврите**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) указывает диапазон кодовых позиций Юникода. |



 

