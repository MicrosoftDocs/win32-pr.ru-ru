---
title: Перечисления DirectWrite
description: DirectWrite определяет следующие перечисления.
ms.assetid: 809ccacd-ff23-4d7b-a177-e7a9937c0c5a
keywords:
- DirectWrite, перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf26901583a84e34d64a2a1c72fdfa17bbc903b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587930"
---
# <a name="directwrite-enumerations"></a>Перечисления DirectWrite

DirectWrite определяет следующие перечисления.

## <a name="in-this-section"></a>В этом разделе

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes"><strong>DWRITE_AUTOMATIC_FONT_AXES</strong></a></td>
<td>Определяет константы, указывающие определенные оси, которые могут применяться автоматически в макете во время выбора шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a> содержит значения, указывающие базовый уровень выравнивания текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition"><strong>DWRITE_BREAK_CONDITION</strong></a></td>
<td>Указывает условие на краях встроенного объекта или текста, используемого для определения поведения разрыва строки.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type"><strong>DWRITE_CONTAINER_TYPE</strong></a></td>
<td>Задает формат контейнера для ресурса шрифта. Формат контейнера отличается от формата файла шрифта (DWRITE_FONT_FILE_TYPE), так как контейнер описывает контейнер, в котором упакован файл шрифта. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE</strong></a></td>
<td>Указывает тип объекта фабрики DirectWrite.</td>
</tr>
<tr>
<td><a href="/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE (Двритекоре)</strong></a></td>
<td>Указывает тип объекта фабрики DirectWrite.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction"><strong>DWRITE_FLOW_DIRECTION</strong></a></td>
<td>Указывает направление размещения строк текста относительно друг друга. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes"><strong>DWRITE_FONT_AXIS_ATTRIBUTES</strong></a></td>
<td>Определяет константы, определяющие атрибуты для оси шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag"><strong>DWRITE_FONT_AXIS_TAG</strong></a></td>
<td>Определяет константы, указывающие идентификатор из четырех символов для оси шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type"><strong>DWRITE_FONT_FACE_TYPE</strong></a></td>
<td>Указывает формат файла для полного начертания шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model"><strong>DWRITE_FONT_FAMILY_MODEL</strong></a></td>
<td>Определяет константы, указывающие, как объединяются семейства шрифтов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag"><strong>DWRITE_FONT_FEATURE_TAG</strong></a></td>
<td>Значение, указывающее типографскую функцию текста, предоставленного шрифтом.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type"><strong>DWRITE_FONT_FILE_TYPE</strong></a></td>
<td>Тип шрифта, представленного одним файлом шрифта. Форматы шрифтов, состоящие из нескольких файлов, например, введите 1. ПФМ и. ПФБ имеют отдельные перечисляемые значения для каждого типа файлов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage"><strong>DWRITE_FONT_LINE_GAP_USAGE</strong></a></td>
<td>Укажите, должно ли значение <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics"><strong>DWRITE_FONT_METRICS</strong></a>:: линегап быть частью метрик линии</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id"><strong>DWRITE_FONT_PROPERTY_ID</strong></a></td>
<td>Определяет строку в шрифте.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations"><strong>DWRITE_FONT_SIMULATIONS</strong></a></td>
<td>Задает моделирование алгоритма, применяемого к начертанию шрифта. Модели с полужирным и наклонным начертанием можно комбинировать с помощью битовой операции OR.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type"><strong>DWRITE_FONT_SOURCE_TYPE</strong></a></td>
<td>Определяет константы, указывающие механизм, с помощью которого шрифт был добавлен в набор шрифтов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch"><strong>DWRITE_FONT_STRETCH</strong></a></td>
<td>Представляет степень, до которой шрифт был растянут по сравнению с нормальным пропорциями шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style"><strong>DWRITE_FONT_STYLE</strong></a></td>
<td>Представляет стиль начертания шрифта: обычный, курсив или наклонный.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight"><strong>DWRITE_FONT_WEIGHT</strong></a></td>
<td>Представляет плотность гарнитуры с точки зрения яркости или плотности штрихов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats"><strong>DWRITE_GLYPH_IMAGE_FORMATS</strong></a></td>
<td>Указывает, какие форматы поддерживаются в шрифте либо на уровне шрифта, либо на глифе.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a> содержит значения, определяющие ориентацию глифа по оси x.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode"><strong>DWRITE_GRID_FIT_MODE</strong></a></td>
<td>Указывает, следует ли включить размещение контуров глифов в сетке (также называемое указанием).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id"><strong>DWRITE_INFORMATIONAL_STRING_ID</strong></a></td>
<td>Перечисление информационной строки, которое определяет строку, внедренную в файл шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method"><strong>DWRITE_LINE_SPACING_METHOD</strong></a></td>
<td>Метод, используемый для межстрочного расстояния в макете текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality"><strong>DWRITE_LOCALITY</strong></a></td>
<td>Указывает расположение ресурса.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode"><strong>DWRITE_MEASURING_MODE</strong></a></td>
<td>Указывает метод измерения, используемый для макета текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method"><strong>DWRITE_NUMBER_SUBSTITUTION_METHOD</strong></a></td>
<td>Указывает, как применять подстановку чисел к цифрам и связанным знакам препинания.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_optical_alignment"><strong>DWRITE_OPTICAL_ALIGNMENT</strong></a></td>
<td>Режим оптического выравнивания полей.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a> содержит значения, указывающие политику, используемую методом <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode"><strong>IDWriteFontFace1:: жетрекоммендедрендерингмоде</strong></a> , чтобы определить, следует ли отображать глифы в режиме структуры.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a> содержит значения, определяющие стиль завершения и округления леттерформс для текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a> содержит значения, указывающие отношение ширины и высоты знака.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a> содержит значения, указывающие сведения о соотношении ширины и высоты знака.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a> содержит значения, указывающие тип символов, доступных в шрифте.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a> содержит значения, указывающие отношение между толстой и самой тонкой точкой штриха для буквы, такой как прописная буква "O".</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a> содержит значения, указывающие общий вид начертания символа.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a> содержит значения, указывающие общие характеристики фигуры шрифта.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a> содержит значения, указывающие тип классификации гарнитуры.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a> содержит значения, указывающие тип заполнения и обработки строки.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a> содержит значения, которые определяют, как заканчивается символ и считанные мгновения ascends.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a> содержит значения, определяющие округление леттерформ для текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a> содержит значения, определяющие обработку контура для декоративных гарнитур.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a> содержит значения, указывающие сведения о размещении заполнение нажатием клавиши в верхнем регистре и обработке диагональных апексес.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a> содержит значения, указывающие пропорции фигуры глифов, учитывая дополнительные сведения о стандартных символах.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a> содержит значения, указывающие общий вид начертания символа с учетом его наклона и хвостов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a> содержит значения, указывающие топологию леттерформс.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a> содержит значения, определяющие внешний вид текста с засечками.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a> содержит значения, указывающие интервал между символами (пробельные и пропорциональные).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a> содержит значения, указывающие связь между тонкими и толстыми фрагментами текстовых символов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a> содержит значения, указывающие пропорции символьных символов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a> содержит значения, указывающие тип набора символов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a> содержит значения, указывающие тип инструмента, используемого для создания форм символов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a> содержит значения, определяющие вес символов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a> содержит значения, указывающие относительный размер строчных букв.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a> содержит значения, указывающие сведения о относительном размере строчных букв и обработке диакритических знаков (ксхеигхт).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment"><strong>DWRITE_PARAGRAPH_ALIGNMENT</strong></a></td>
<td>Задает выравнивание текста абзаца вдоль оси направления потока относительно верхней и нижней части поля макета потока. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry"><strong>DWRITE_PIXEL_GEOMETRY</strong></a></td>
<td>Представляет внутреннюю структуру пикселя устройства (то есть физическое расположение красного, зеленого и синего цветовых компонентов), которое предполагается для отрисовки текста. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction"><strong>DWRITE_READING_DIRECTION</strong></a></td>
<td>Указывает направление чтения. 
<blockquote>
[!Note]<br />
<strong>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</strong> и <strong>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</strong> доступны только в Windows 8.1 и более поздних версиях.
</blockquote>
</td>
</tr>
<tr>
<td><a href="/windows/win32/directwrite/dwrite-rendering-mode-enumerations">Перечисления DWRITE_RENDERING_MODE</a></td>
<td>Начиная с Windows 8, перечисление <strong>DWRITE_RENDERING_MODE</strong> добавило новые значения перечисления и не является устаревшим для других.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1"><strong>DWRITE_RENDERING_MODE1</strong></a></td>
<td>Указывает способ отображения глифов.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_script_shapes"><strong>DWRITE_SCRIPT_SHAPES</strong></a></td>
<td>Указывает дополнительные требования к формированию текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment"><strong>DWRITE_TEXT_ALIGNMENT</strong></a></td>
<td>Задает выравнивание текста абзаца вдоль оси направления чтения относительно начального и конечного краев поля макета.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a> содержит значения, указывающие тип сглаживания, используемого для текста, когда режим рендеринга вызывает для сглаживания.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type"><strong>DWRITE_TEXTURE_TYPE</strong></a></td>
<td>Определяет тип текстуры альфа.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity"><strong>DWRITE_TRIMMING_GRANULARITY</strong></a></td>
<td>Задает гранулярность текста, используемую для сокращения размеров текста, передающего поле макета.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a></td>
<td>Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a> содержит значения, указывающие желаемый тип ориентации глифов для текста.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping"><strong>DWRITE_WORD_WRAPPING</strong></a></td>
<td>Задает перенос по словам для использования в определенном многострочном абзаце. 
<blockquote>
[!Note]<br />
<strong>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</strong>, <strong>DWRITE_WORD_WRAPPING_WHOLE _WORD</strong>и <strong>DWRITE_WORD_WRAPPING_CHARACTER</strong> доступны только в Windows 8.1 и более поздних версиях.
</blockquote>
</td>
</tr>
</tbody>
</table>



 

 

 





