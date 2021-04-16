---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Вмсдкидл. h)
description: Переход прямоугольника показывает новое изображение в прямоугольнике внутри фрейма.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708418"
---
# <a name="wmt_videoimage_transition_rectangle"></a>\_ \_ прямоугольник перехода ВМТ \_ видеоимаже

Переход прямоугольника показывает новое изображение в прямоугольнике внутри фрейма.

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
<td>Координата по оси X относительно видеокадра центра прямоугольника.</td>
</tr>
<tr class="even">
<td>Центр по оси Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Координата по оси Y относительно видеокадра центра прямоугольника.</td>
</tr>
<tr class="odd">
<td>Ширина</td>
<td><strong>fEffectPara2</strong></td>
<td>Ширина прямоугольника в пикселях.</td>
</tr>
<tr class="even">
<td>Высота</td>
<td><strong>fEffectPara3</strong></td>
<td>Высота прямоугольника в пикселях.</td>
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

 

 





