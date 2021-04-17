---
title: Структуры Direct2D
description: Direct2D предоставляет следующие структуры. Дополнительные структуры определяются в пространстве имен D2D1.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4b668e143b3ab5b166582e504c68a05722da7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681620"
---
# <a name="direct2d-structures"></a>Структуры Direct2D

Direct2D предоставляет следующие структуры. Дополнительные структуры определяются в [пространстве имен D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**\_Цветовая \_ F D2D**](d2d-color-f.md) | Описывает красный, зеленый, синий и альфа-компоненты цвета. |
| [**\_Матрица D2D \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Представляет матрицу размером 3 на 2. |
| [**\_Матрица D2D \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Описывает матрицу с плавающей точкой 4 по 3. |
| [**\_Матрица D2D \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Описывает матрицу с плавающей точкой 4 по 4. |
| [**\_Матрица D2D \_ 5x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Описывает матрицу с плавающей точкой 5 по 4. |
| [**\_Точка D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Представляет пару координат x и y, выраженную в виде значений с плавающей запятой в двухмерном пространстве. |
| [**\_2L точки \_ D2D**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | \_Структура 2L точки постоянного тока \_ определяет координаты x и y точки. |
| [**Точка D2D с \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Представляет пару координат x и y, выраженную в виде значения 32-разрядного целого числа без знака в двухмерном пространстве. |
| [**D2D, \_ прямоугольник \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Представляет прямоугольник, определяемый координатами верхнего левого угла (слева, сверху) и координатами правого нижнего угла (справа, снизу).  |
| [**D2D, \_ прямоугольник \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | Структура [**D2D \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) определяет координаты верхнего левого и нижнего правого угла прямоугольника. |
| [**D2D ( \_ Rect) \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Представляет прямоугольник, определяемый верхней левой угловой парой координат (слева, сверху) и нижней правой угловой парой координат (справа, снизу). Эти координаты выражаются как 32-разрядные целочисленные значения. |
| [**\_Размер D2D \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Сохраняет упорядоченную пару значений с плавающей запятой, обычно ширину и высоту прямоугольника.  |
| [**\_Размер D2D \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Сохраняет упорядоченную пару целых чисел — обычно ширину и высоту прямоугольника. |
| [**\_Экземпляр D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Двумерный вектор, состоящий из двух значений с плавающей запятой одиночной точности (x, y).  |
| [**\_3F вектора D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Трехмерный вектор, состоящий из трех значений с плавающей запятой одиночной точности (x, y, z). |
| [**\_4F вектора D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Вектор 4D, состоящий из четырех значений с плавающей запятой одиночной точности (x, y, z, w). |
| [**\_Сегмент дуги \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Описывает эллиптическую дугу между двумя точками. |
| [**\_Сегмент Безье \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Представляет сегмент Безье третьего порядка, нарисованный между двумя точками. |
| [**\_Свойства кисти точечного рисунка D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Описывает режимы расширения и режим интерполяции [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_ \_ PROPERTIES1ная КИСТь D2D1 \_**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Описывает режимы расширения и режим интерполяции [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_Свойства битовой карты D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Описывает формат пикселей и DPI точечного рисунка. |
| [**\_Точечный рисунок D2D1 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Эта структура позволяет создавать [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) с параметрами битовой карты и сведениями о контексте цвета.  |
| [**\_Описание D2D1 Blend \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Определяет описание смешения, которое будет использоваться в определенном преобразовании Blend. |
| [**\_Свойства кисти \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Описывает непрозрачность и Преобразование кисти. |
| [**D2D1 \_ Color \_ F**](d2d1-color-f.md) | Описывает красный, зеленый, синий и альфа-компоненты цвета. |
| [**\_Свойства создания \_ D2D1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | Задает параметры, с помощью которых создается [Direct2D](./direct2d-portal.md) устройство, фабрика и контекст устройства.  |
| [**\_Свойства пользовательского \_ \_ буфера вершин \_ D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Определяет шейдер вершин и описание элемента ввода для определения макета входных данных. |
| [**\_ \_ Описание состояния рисования \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Описывает состояние прорисовки целевого объекта отрисовки.  |
| [**D2D1 \_ \_ DESCRIPTION1 состояния \_ рисования**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Описывает состояние отображения контекста устройства. |
| [**\_ \_ Описание входного действия D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Описывает функции влияния. |
| [**\_Эллипс D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Содержит центральную точку, x-радиус и y-радиус эллипса. |
| [**\_Варианты фабрики D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Содержит уровень отладки объекта [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .  |
| [**D2D1 \_ данных о функциях \_ \_ Double**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Описывает поддержку Double в шейдерах. |
| [**\_ \_ \_ \_ \_ Параметры оборудования D3D10 X D2D1 данных \_ компонентов**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Описывает поддержку функций шейдера вычислений, которая является параметром на уровне компонентов D3D10. |
| [**\_Исправление сетки градиента D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Представляет исправление тензорные с 16 контрольными точками, четырьмя цветами угла и флагами границ. ID2D1GradientMesh состоит из одного или нескольких исправлений сетки градиента. Чтобы создать ее, используйте [**функцию градиентмешпатч**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) или [**функцию градиентмешпатчфромкунспатч**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) .  |
| [**D2D1 \_ градиента \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Содержит расположение и цвет ограничителя градиента.  |
| [**\_ \_ \_ Свойства целевого объекта прорисовки D2D1 HWND \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Содержит HWND, размер пикселей и параметры представления для [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget). |
| [**\_Свойства стиля рукописного ввода D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Определяет общую форму кончика пера и преобразование, используемое в объекте [**ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle) .  |
| [**\_ \_ Свойства кисти изображения \_ D2D1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Описывает функции кисти изображений. |
| [**\_ \_ Сегмент Безье D2D1ов \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Представляет сегмент Безье, используемый при создании объекта [**ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) . Эта структура отличается от [**\_ \_ сегмента Безье D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) в том, что он состоит из [**D2D1 \_ перьевых \_ точек**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point), которые содержат радиус в дополнение к координатам x и y.  |
| [**\_Точка рукописного ввода D2D1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Представляет точку, пару радиусов, составляющую часть [**\_ \_ \_ сегмента Безье D2D1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment). |
| [**\_Описание входных данных D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Описывает параметры, которые могут быть заданы на текстурах ввода. |
| [**\_Элемент ввода D2D1, \_ \_ DESC**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Описание одного элемента в макете вершины. |
| [**\_Параметры слоя \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Содержит границы содержимого, сведения о маске, параметры непрозрачности и другие параметры для ресурса слоя.  |
| [**D2D1 \_ Layer \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Содержит границы содержимого, сведения о маске, параметры непрозрачности и другие параметры для ресурса слоя. |
| [**\_Свойства кисти линейного \_ ГРАДИЕНТа D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Содержит начальную точку и конечную точку оси градиента для [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).  |
| [**D2D1 \_ Матрица \_ 3X2 \_ F**](d2d1-matrix-3x2-f.md) | Представляет матрицу размером 3 на 2.  |
| [**D2D1 \_ Матрица \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | Представляет матрицу 4 на 3.  |
| [**\_Матрица D2D1 \_ 4x4 \_ F**](d2d1-matrix-4x4-f.md) | Представляет матрицу 4 по 4.  |
| [**D2D1 \_ Матрица \_ 5x4 \_ F**](d2d1-matrix-5x4-f.md) | Представляет матрицу с 5 по 4.  |
| [**D2D1 \_ сопоставленный \_ Rect**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Описывает сопоставленную память из API [**ID2D1Bitmap1:: Map**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) . |
| [**\_Формат ПИКСЕЛЕЙ \_ D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Содержит формат данных и альфа-режим для точечного рисунка или целевого объекта прорисовки.  |
| [**D2D1 \_ точка \_ 2F**](d2d1-point-2f.md) | Представляет пару координат x и y в двухмерном пространстве. |
| [**D2D1 \_ точка \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | Структура POINT определяет координаты x и y точки. |
| [**D2D1 \_ точка \_ 2U**](d2d1-point-2u.md) | Представляет пару координат x и y в двухмерном пространстве.  |
| [**\_Описание точки \_ D2D1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Описывает точку на геометрии контура. |
| [**\_ \_ Свойства элемента управления ПЕЧАТЬю D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | Свойства создания для объекта [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) . |
| [**\_Привязка свойства \_ D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Определяет привязку свойства к паре функций, которые получают и задают соответствующее свойство.  |
| [**\_ \_ Сегмент Безье D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Содержит контрольную точку и конечную точку для сегмента Безье квадратичных кривых. |
| [**\_Свойства кисти радиального \_ ГРАДИЕНТа D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Содержит смещение источника градиента и размер и положение эллипса градиента для [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).  |
| [**D2D1 \_ Rect \_ F**](d2d1-rect-f.md) | Представляет прямоугольник, определяемый координатами верхнего левого угла (слева, сверху) и координатами правого нижнего угла (справа, снизу).  |
| [**D2D1 \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | Структура RECT определяет координаты левого верхнего и правого нижнего угла прямоугольника. |
| [**D2D1 \_ Rect \_ U**](d2d1-rect-u.md) | Представляет прямоугольник, определяемый координатами верхнего левого угла (слева, сверху) и координатами правого нижнего угла (справа, снизу).  |
| [**\_ \_ Свойства текстуры ресурса \_ D2D1**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Определяет текстуру ресурсов при создании исходной текстуры ресурса. |
| [**\_Использование ресурсов \_ D2D1**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Описывает память, используемую текстурами и шейдерами изображений. |
| [**\_ \_ Свойства целевого объекта ПРОРИСОВКи D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Содержит параметры отрисовки (оборудование или программное обеспечение), формат пикселей, сведения о DPI, параметры удаленного взаимодействия и требования поддержки Direct3D для целевого объекта прорисовки.  |
| [**\_Элементы управления отрисовкой D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Описывает ограничения, применяемые к модулю визуализации эффектов работы с образами. |
| [**D2D1 \_ Скругленный \_ прямоугольник**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Содержит размеры и угловые радиусы скругленного прямоугольника. |
| [**\_Простой \_ цветовой \_ профиль D2D1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Простое описание цветового пространства. |
| [**D2D1 \_ размер \_ F**](d2d1-size-f.md) | Сохраняет упорядоченную пару с плавающей запятой, обычно ширину и высоту прямоугольника. |
| [**D2D1 \_ размер \_ U**](d2d1-size-u.md) | Сохраняет упорядоченную пару целых чисел — обычно ширину и высоту прямоугольника. |
| [**\_ \_ Свойства стиля D2D1 \_ Stroke**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Описывает штрих, который обозначает фигуру.  |
| [**D2D1 \_ , \_ стиль обводки \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Описывает штрих, который обозначает фигуру. |
| [**\_Длина D2D1 SVG \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Представляет длину SVG. |
| [**D2D1 \_ SVG \_ сохранять \_ пропорции \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Представляет все параметры SVG Пресервеаспектратио. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Представляет viewBox SVG. |
| [**\_Свойства источника преобразованного \_ изображения \_ D2D1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Свойства источника преобразованного изображения. |
| [**D2D1 \_ треугольник**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Содержит три вершины, описывающие треугольник. |
| [**D2D1 \_ vector \_**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Вектор из двух значений с плавающей запятой (x, y). |
| [**D2D1 \_ vector \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Вектор из 3 значений с плавающей запятой (x, y, z). |
| [**D2D1 \_ vector \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Вектор из 4 значений с плавающей запятой (x, y, z, w). |
| [**\_ \_ Свойства буфера вершин \_ D2D1**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Определяет свойства буфера вершин, которые являются стандартными для всех определений вершинных шейдеров. |
| [**\_Диапазон ВЕРШИН \_ D2D1**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Определяет диапазон вершин, используемых при отрисовке меньшего, чем полного содержимого буфера вершин. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Хранит сведения о цвете и альфа-канале. |
| [*\_ \_ Фабрика эффектов PD2D1*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Описывает реализацию воздействия. |