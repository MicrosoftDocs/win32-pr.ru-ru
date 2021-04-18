---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Вмсдкидл. h)
description: При переходе типа "звезда" новый образ отображается на пять звездочек внутри рамки.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704399"
---
# <a name="wmt_videoimage_transition_star"></a>ВМТ \_ видеоимаже \_ 1-2-3 \_

При переходе типа "звезда" новый образ отображается на пять звездочек внутри рамки.

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
<td>Координата по оси X относительно видеокадра центра звезды.</td>
</tr>
<tr class="even">
<td>Центр по оси Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Координата по оси Y относительно видеокадра центра звезды.</td>
</tr>
<tr class="odd">
<td>Радиус.</td>
<td><strong>fEffectPara2</strong></td>
<td>Радиус (в пикселях) круга, определяемый точками звезды.</td>
</tr>
<tr class="even">
<td>Композиция</td>
<td><strong>fEffectPara3</strong></td>
<td>Задайте одно из следующих значений:
<ul>
<li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li>
<li>1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li>
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

 

 





