---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Вмсдкидл. h)
description: Переход на слайд показывает новое изображение путем перемещения старого изображения из рамки.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648705"
---
# <a name="wmt_videoimage_transition_slide"></a>\_ \_ слайд перехода ВМТ \_ видеоимаже

Переход на слайд показывает новое изображение путем перемещения старого изображения из рамки.

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
<td>расстояние;</td>
<td><strong>fEffectPara0</strong></td>
<td>Расстояние (в пикселях), в котором старое изображение слайдов выходит за пределы рамки.</td>
</tr>
<tr class="even">
<td>Направление</td>
<td><strong>fEffectPara1</strong></td>
<td>Направление, в котором слайды старого изображения. Задайте одно из следующих значений:<br/>
<ul>
<li>0 — слайд справа.</li>
<li>1 — слайд слева.</li>
<li>2. Проведите вверх.</li>
<li>3. Проведите вниз.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Композиция</td>
<td><strong>fEffectPara2</strong></td>
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

 

 





