---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Вмсдкидл. h)
description: Переход вставки показывает новый рисунок в прямоугольнике, который начинается с одного угла рамки.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f815e0bb1fc7e8e1cba277f68b7950af2b20395092b69b2c07ebb7ac51367da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843793"
---
# <a name="wmt_videoimage_transition_inset"></a>ВМТ \_ видеоимаже \_ перехода \_

Переход вставки показывает новый рисунок в прямоугольнике, который начинается с одного угла рамки.

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
<td>Ширина</td>
<td><strong>fEffectPara0</strong></td>
<td>Ширина отступа в пикселях.</td>
</tr>
<tr class="even">
<td>Высота</td>
<td><strong>fEffectPara1</strong></td>
<td>Высота отступа в пикселях.</td>
</tr>
<tr class="odd">
<td>Направление</td>
<td><strong>fEffectPara2</strong></td>
<td>Угол, с которого начинается вставка. Задайте одно из следующих значений:<br/>
<ul>
<li>0-вниз слева</li>
<li>1 — нижний правый</li>
<li>2-верхний левый</li>
<li>3 — верхний правый</li>
</ul></td>
</tr>
<tr class="even">
<td>Композиция</td>
<td><strong>fEffectPara3</strong></td>
<td>Задайте одно из следующих значений:
<ul>
<li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li>
<li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





