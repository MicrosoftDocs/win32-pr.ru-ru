---
title: перечисления DirectWrite
description: DirectWrite определяет следующие перечисления.
ms.assetid: 809ccacd-ff23-4d7b-a177-e7a9937c0c5a
keywords:
- DirectWrite, перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71edfe3f60bb3ae2568c38d92352c62b6890721e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468181"
---
# <a name="directwrite-enumerations"></a>перечисления DirectWrite

DirectWrite определяет следующие перечисления.

## <a name="in-this-section"></a>В этом разделе


| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes"><strong>DWRITE_AUTOMATIC_FONT_AXES</strong></a> | Определяет константы, указывающие определенные оси, которые могут применяться автоматически в макете во время выбора шрифта. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a> содержит значения, указывающие базовый уровень выравнивания текста. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition"><strong>DWRITE_BREAK_CONDITION</strong></a> | Указывает условие на краях встроенного объекта или текста, используемого для определения поведения разрыва строки. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type"><strong>DWRITE_CONTAINER_TYPE</strong></a> | Задает формат контейнера для ресурса шрифта. Формат контейнера отличается от формата файла шрифта (DWRITE_FONT_FILE_TYPE), так как контейнер описывает контейнер, в котором упакован файл шрифта.  | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE</strong></a> | указывает тип объекта фабрики DirectWrite. | 
| <a href="/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE (Двритекоре)</strong></a> | указывает тип объекта фабрики DirectWrite. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction"><strong>DWRITE_FLOW_DIRECTION</strong></a> | Указывает направление размещения строк текста относительно друг друга.  | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes"><strong>DWRITE_FONT_AXIS_ATTRIBUTES</strong></a> | Определяет константы, определяющие атрибуты для оси шрифта. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag"><strong>DWRITE_FONT_AXIS_TAG</strong></a> | Определяет константы, указывающие идентификатор из четырех символов для оси шрифта. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type"><strong>DWRITE_FONT_FACE_TYPE</strong></a> | Указывает формат файла для полного начертания шрифта. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model"><strong>DWRITE_FONT_FAMILY_MODEL</strong></a> | Определяет константы, указывающие, как объединяются семейства шрифтов. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag"><strong>DWRITE_FONT_FEATURE_TAG</strong></a> | Значение, указывающее типографскую функцию текста, предоставленного шрифтом. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type"><strong>DWRITE_FONT_FILE_TYPE</strong></a> | Тип шрифта, представленного одним файлом шрифта. Форматы шрифтов, состоящие из нескольких файлов, например, введите 1. ПФМ и. ПФБ имеют отдельные перечисляемые значения для каждого типа файлов. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage"><strong>DWRITE_FONT_LINE_GAP_USAGE</strong></a> | Укажите, должно ли значение <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics"><strong>DWRITE_FONT_METRICS</strong></a>:: линегап быть частью метрик линии | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id"><strong>DWRITE_FONT_PROPERTY_ID</strong></a> | Определяет строку в шрифте. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations"><strong>DWRITE_FONT_SIMULATIONS</strong></a> | Задает моделирование алгоритма, применяемого к начертанию шрифта. Модели с полужирным и наклонным начертанием можно комбинировать с помощью битовой операции OR. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type"><strong>DWRITE_FONT_SOURCE_TYPE</strong></a> | Определяет константы, указывающие механизм, с помощью которого шрифт был добавлен в набор шрифтов. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch"><strong>DWRITE_FONT_STRETCH</strong></a> | Представляет степень, до которой шрифт был растянут по сравнению с нормальным пропорциями шрифта. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style"><strong>DWRITE_FONT_STYLE</strong></a> | Представляет стиль начертания шрифта: обычный, курсив или наклонный. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight"><strong>DWRITE_FONT_WEIGHT</strong></a> | Представляет плотность гарнитуры с точки зрения яркости или плотности штрихов. | 
| <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats"><strong>DWRITE_GLYPH_IMAGE_FORMATS</strong></a> | Указывает, какие форматы поддерживаются в шрифте либо на уровне шрифта, либо на глифе. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a> содержит значения, определяющие ориентацию глифа по оси x. | 
| <a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode"><strong>DWRITE_GRID_FIT_MODE</strong></a> | Указывает, следует ли включить размещение контуров глифов в сетке (также называемое указанием). | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id"><strong>DWRITE_INFORMATIONAL_STRING_ID</strong></a> | Перечисление информационной строки, которое определяет строку, внедренную в файл шрифта. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method"><strong>DWRITE_LINE_SPACING_METHOD</strong></a> | Метод, используемый для межстрочного расстояния в макете текста. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality"><strong>DWRITE_LOCALITY</strong></a> | Указывает расположение ресурса. | 
| <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode"><strong>DWRITE_MEASURING_MODE</strong></a> | Указывает метод измерения, используемый для макета текста. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method"><strong>DWRITE_NUMBER_SUBSTITUTION_METHOD</strong></a> | Указывает, как применять подстановку чисел к цифрам и связанным знакам препинания. | 
| <a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_optical_alignment"><strong>DWRITE_OPTICAL_ALIGNMENT</strong></a> | Режим оптического выравнивания полей. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a> содержит значения, указывающие политику, используемую методом <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode"><strong>IDWriteFontFace1:: жетрекоммендедрендерингмоде</strong></a> , чтобы определить, следует ли отображать глифы в режиме структуры. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a> содержит значения, определяющие стиль завершения и округления леттерформс для текста. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a> содержит значения, указывающие отношение ширины и высоты знака. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a> содержит значения, указывающие сведения о соотношении ширины и высоты знака. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a> содержит значения, указывающие тип символов, доступных в шрифте. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a> содержит значения, указывающие отношение между толстой и самой тонкой точкой штриха для буквы, такой как прописная буква "O". | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a> содержит значения, указывающие общий вид начертания символа. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a> содержит значения, указывающие общие характеристики фигуры шрифта. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a> содержит значения, указывающие тип классификации гарнитуры. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a> содержит значения, указывающие тип заполнения и обработки строки. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a> содержит значения, которые определяют, как заканчивается символ и считанные мгновения ascends. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a> содержит значения, определяющие округление леттерформ для текста. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a> содержит значения, определяющие обработку контура для декоративных гарнитур. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a> содержит значения, указывающие сведения о размещении заполнение нажатием клавиши в верхнем регистре и обработке диагональных апексес. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a> содержит значения, указывающие пропорции фигуры глифов, учитывая дополнительные сведения о стандартных символах. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a> содержит значения, указывающие общий вид начертания символа с учетом его наклона и хвостов. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a> содержит значения, указывающие топологию леттерформс. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a> содержит значения, определяющие внешний вид текста с засечками. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a> содержит значения, указывающие интервал между символами (пробельные и пропорциональные). | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a> содержит значения, указывающие связь между тонкими и толстыми фрагментами текстовых символов. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a> содержит значения, указывающие пропорции символьных символов. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a> содержит значения, указывающие тип набора символов. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a> содержит значения, указывающие тип инструмента, используемого для создания форм символов. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a> содержит значения, определяющие вес символов. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a> содержит значения, указывающие относительный размер строчных букв. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a> содержит значения, указывающие сведения о относительном размере строчных букв и обработке диакритических знаков (ксхеигхт). | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment"><strong>DWRITE_PARAGRAPH_ALIGNMENT</strong></a> | Задает выравнивание текста абзаца вдоль оси направления потока относительно верхней и нижней части поля макета потока.  | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry"><strong>DWRITE_PIXEL_GEOMETRY</strong></a> | Представляет внутреннюю структуру пикселя устройства (то есть физическое расположение красного, зеленого и синего цветовых компонентов), которое предполагается для отрисовки текста.  | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction"><strong>DWRITE_READING_DIRECTION</strong></a> | Указывает направление чтения. <blockquote>[!Note]<br /><strong>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</strong> и <strong>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</strong> доступны только в Windows 8.1 и более поздних версиях.</blockquote> | 
| <a href="/windows/win32/directwrite/dwrite-rendering-mode-enumerations">Перечисления DWRITE_RENDERING_MODE</a> | начиная с Windows 8, перечисление <strong>DWRITE_RENDERING_MODE</strong> добавило новые значения перечисления и нерекомендуемые другие. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1"><strong>DWRITE_RENDERING_MODE1</strong></a> | Указывает способ отображения глифов. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_script_shapes"><strong>DWRITE_SCRIPT_SHAPES</strong></a> | Указывает дополнительные требования к формированию текста. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment"><strong>DWRITE_TEXT_ALIGNMENT</strong></a> | Задает выравнивание текста абзаца вдоль оси направления чтения относительно начального и конечного краев поля макета. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a> содержит значения, указывающие тип сглаживания, используемого для текста, когда режим рендеринга вызывает для сглаживания. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type"><strong>DWRITE_TEXTURE_TYPE</strong></a> | Определяет тип текстуры альфа. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity"><strong>DWRITE_TRIMMING_GRANULARITY</strong></a> | Задает гранулярность текста, используемую для сокращения размеров текста, передающего поле макета. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a> | Перечисление <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a> содержит значения, указывающие желаемый тип ориентации глифов для текста. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping"><strong>DWRITE_WORD_WRAPPING</strong></a> | Задает перенос по словам для использования в определенном многострочном абзаце. <blockquote>[!Note]<br /><strong>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</strong>, <strong>DWRITE_WORD_WRAPPING_WHOLE _WORD</strong>и <strong>DWRITE_WORD_WRAPPING_CHARACTER</strong> доступны только в Windows 8.1 и более поздних версиях.</blockquote> | 




 

 

 





