---
description: Различные флаги примитивной возможности драйвера.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343139"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Различные флаги примитивной возможности драйвера.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#определенно</td>
<td>Значение</td>
<td>Описание</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>Устройство может включать и отключать изменение буфера глубины в операциях с пикселами.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>Драйвер не выполняет отбор треугольников. Соответствует элементу D3DCULL_NONE перечислимого типа <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>Драйвер поддерживает истечение треугольника по часовой стрелке в состоянии D3DRS_CULLMODE. (Это относится только к примитивам треугольника.) Этот флаг соответствует элементу D3DCULL_CW перечисляемого типа <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>Драйвер поддерживает истечение против часовой стрелки в состоянии D3DRS_CULLMODE. (Это относится только к примитивам треугольника.) Этот флаг соответствует элементу D3DCULL_CCW перечисляемого типа <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>Устройство поддерживает операции записи на канал для буфера цвета целевого объекта рендеринга с помощью состояния D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>Устройство правильно выводит масштабируемые точки размером больше 1,0 в определяемые пользователем отрезкиные плоскости.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Зажимы устройств после преобразования-примитивы вершин. Укажите D3DUSAGE_DONOTCLIP, если конвейер не должен выполнять отсечение. В этом случае может потребоваться дополнительная обрезка программного обеспечения во время рисования, требующая, чтобы буфер вершин наводился в системной памяти.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>Устройство поддерживает <a href="d3dta.md">D3DTA</a> для временного регистра.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>Устройство поддерживает операции альфа-смешения, кроме D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Эталонное устройство, которое не подготавливается к просмотру.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>Устройство поддерживает независимые маски записи для нескольких текстур элементов или нескольких целевых объектов прорисовки.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>Устройство поддерживает константы для каждого этапа. См. D3DTSS_CONSTANT в <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>Устройство поддерживает преобразование в sRGB после смешения. 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>Устройство поддерживает отдельные туманы и бликовые альфа-каналы. Многие устройства используют отраженный альфа-канал для хранения коэффициента тумана.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>Устройство поддерживает отдельные параметры смешения для альфа-канала.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>Устройство поддерживает разные битовые глубины для нескольких целевых объектов рендеринга.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>Устройство поддерживает операции шейдера после пикселей для нескольких целевых объектов рендеринга.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Фактор для зажимов устройства — коэффициент смешения на вершину.</td>
</tr>
</tbody>
</table>



 

Эти константы используются членом Примитивемисккапс объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Сведения о константе



| Требование                         |  Значение          |
|--------------------------|------------|
| Заголовок                   | d3d9caps. h |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
