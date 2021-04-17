---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Вмсдкидл. h)
description: При заполнении V новый рисунок отображается в треугольнике, который начинается с одной стороны рамки.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694568"
---
# <a name="wmt_videoimage_transition_filled_v"></a>ВМТ \_ видеоимаже \_ Переход \_ заполнен \_ V

При заполнении V новый рисунок отображается в треугольнике, который начинается с одной стороны рамки.

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
<td>Ширина заполненной V в пикселях.</td>
</tr>
<tr class="even">
<td>Высота</td>
<td><strong>fEffectPara1</strong></td>
<td>Высота заполненной V в пикселях.</td>
</tr>
<tr class="odd">
<td>Направление</td>
<td><strong>fEffectPara2</strong></td>
<td>Направление, с которого происходит заполнение V. Задайте одно из следующих значений:<br/>
<ul>
<li>0 — переход с левой стороны рамки.</li>
<li>1 — переход с правой стороны рамки.</li>
<li>2 — переходит от нижней части рамки.</li>
<li>3 — переходит от верхней части рамки.</li>
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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





