---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Вмсдкидл. h)
description: Переход с разбиением раскрывает новый образ, разделив старый образ. Разбиение отображается вдоль прямой горизонтальной или вертикальной линии, которая начинается внутри рамки.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648704"
---
# <a name="wmt_videoimage_transition_split"></a>ВМТ \_ видеоимаже \_ Переход на \_ разбиение

Переход с разбиением раскрывает новый образ, разделив старый образ. Разбиение отображается вдоль прямой горизонтальной или вертикальной линии, которая начинается внутри рамки.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Параметр</th>
<th>Член структуры</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Центр по оси X</td>
<td><strong>fEffectPara0</strong></td>
<td>Координата X относительно видеокадра исходной строки разбиения.</td>
</tr>
<tr class="even">
<td>Центр по оси Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Координата по оси Y относительно видеокадра исходной строки разбиения.</td>
</tr>
<tr class="odd">
<td>расстояние;</td>
<td><strong>fEffectPara2</strong></td>
<td>Ширина разбиения в пикселях.</td>
</tr>
<tr class="even">
<td>Направление</td>
<td><strong>fEffectPara3</strong></td>
<td>Ориентация разбиения. Задайте одно из следующих значений:<br/>
<ul>
<li>0 — разделяется вдоль горизонтальной линии.</li>
<li>1 — разбивается вдоль вертикальной линии.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Композиция</td>
<td><strong>fEffectPara4</strong></td>
<td>Задайте одно из следующих значений:
<ul>
<li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li>
<li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





