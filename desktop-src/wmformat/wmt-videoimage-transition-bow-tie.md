---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Вмсдкидл. h)
description: Переход «линия бабочки» раскрывает новый образ в наборе треугольников на противоположных сторонах рамки.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f77cd2782bad6e4f83b5a4d1e719b0c21d704fefd2d4cccacfc0690a4fb0fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843955"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>ВМТ \_ видеоимаже \_ Переход на \_ бабочку \_

Переход «линия бабочки» раскрывает новый образ в наборе треугольников на противоположных сторонах рамки.

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
<td>Ширина каждой треугольной стороны для привязки бабочки.</td>
</tr>
<tr class="even">
<td>Высота</td>
<td><strong>fEffectPara1</strong></td>
<td>Высота каждой треугольной стороны привязку к бабочке.</td>
</tr>
<tr class="odd">
<td>Направление</td>
<td><strong>fEffectPara2</strong></td>
<td>Задайте одно из следующих значений:
<ul>
<li>0 — задает результат горизонтальной бабочки, в котором треугольники вводятся справа и слева от рамки.</li>
<li>1 — задает действие по вертикали, при котором треугольники вводятся сверху и снизу рамки.</li>
</ul></td>
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
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





