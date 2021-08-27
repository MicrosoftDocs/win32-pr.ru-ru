---
title: ID2D1SvgElement GetAttributeValue методы
description: Возвращает атрибут этого элемента.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Методы GetAttributeValue Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cfc85f2af132c52a95f196aa6e0722b4d75ccc9bc8a4b7a1abb992cc581a6f32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076854"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>Методы ID2D1SvgElement:: GetAttributeValue

Возвращает атрибут этого элемента.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                     | Описание                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue (ПКВСТР, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Возвращает атрибут этого элемента в виде числа с плавающей запятой.<br/>                                                                                                    |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ Color \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Возвращает атрибут этого элемента в виде цвета.<br/>                                                                                                    |
| [**GetAttributeValue (ПКВСТР, РЕФИИД, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Возвращает атрибут этого элемента в качестве типа интерфейса. <br/>                                                                                         |
| [**GetAttributeValue (ПКВСТР, \_ режим заполнения \_ D2D1 \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Возвращает атрибут этого элемента в качестве режима заполнения. Этот метод можно использовать для получения значений свойств "Заливка-правило" или "правило обрезки".<br/>             |
| [**GetAttributeValue (ПКВСТР, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Возвращает атрибут этого элемента в виде краски. Этот метод можно использовать для получения значений свойств Fill или Stroke.<br/>                         |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ \_ Длина SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Возвращает атрибут этого элемента в виде значения длины.<br/>                                                                                             |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ \_ Отображение SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Возвращает атрибут этого элемента в виде отображаемого значения. Этот метод можно использовать для получения значения свойства дисплея.<br/>                          |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ \_ -режим расширения \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Возвращает атрибут этого элемента в качестве значения режима расширения. Этот метод можно использовать для получения значения атрибута Спреадмесод.<br/>                  |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ SVG \_ Overflow \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Возвращает атрибут этого элемента в виде значения переполнения. Этот метод можно использовать для получения значения свойства Overflow.<br/>                       |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ с \_ \_ концом строки SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Возвращает атрибут этого элемента в качестве значения конца строки. Этот метод можно использовать для получения значения свойства Stroke-линекап.<br/>                  |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ Matrix \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Возвращает атрибут этого элемента в виде значения матрицы. Этот метод можно использовать для получения значения атрибута Transform или Градиенттрансформ.<br/>     |
| [**GetAttributeValue (ПКВСТР, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Возвращает атрибут этого элемента в виде данных пути. Этот метод можно использовать для получения значения атрибута d в элементе Path.<br/>                   |
| [**GetAttributeValue (ПКВСТР, D2D1ное \_ \_ соединение со строкой SVG \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Возвращает атрибут этого элемента в виде значения соединение строки. Этот метод можно использовать для получения значения свойства Stroke-линежоин.<br/>                |
| [**GetAttributeValue (ПКВСТР, \_ \_ тип единицы SVG \_ D2D1 \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Возвращает атрибут этого элемента в виде значения типа единицы. Этот метод можно использовать для получения значения атрибута Градиентунитс или Клиппасунитс.<br/>  |
| [**GetAttributeValue (ПКВСТР, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Возвращает атрибут этого элемента.<br/>                                                                                                               |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ \_ видимость SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Возвращает атрибут этого элемента в виде значения видимости. Этот метод можно использовать для получения значения свойства Visibility.<br/>                    |
| [**GetAttributeValue (ПКВСТР, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Возвращает атрибут этого элемента в виде массива штрихов штриха. Этот метод можно использовать для получения значения свойства Stroke-дашаррай.<br/>             |
| [**GetAttributeValue (ПКВСТР, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Возвращает атрибут этого элемента в виде точек. Этот метод можно использовать для получения значения атрибута Points на многоугольнике или элементе ломаной линии.<br/>  |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ Сохранение пропорций SVG \_ \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Возвращает атрибут этого элемента в виде значения сохранения пропорций. Этот метод можно использовать для получения значения атрибута Пресервеаспектратио.<br/> |
| [**GetAttributeValue (ПКВСТР, D2D1 \_ \_ атрибут SVG \_ \_ , тип POD, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Возвращает атрибут этого элемента в виде типа POD.<br/>                                                                                                 |
| [**GetAttributeValue (ПКВСТР, \_ \_ тип строки атрибута SVG D2D1 \_ \_ , пвстр, UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Возвращает атрибут этого элемента в виде строки. <br/>                                                                                                  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

