---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Вмсдкидл. h)
description: Переход ромба открывает новый образ в ромбе.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af271c220fc48924905a067336a438baec1ef0ac4b2dca1b266d3ea77d665f71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653285"
---
# <a name="wmt_videoimage_transition_diamond"></a>ВМТ \_ видеоимаже \_ Переход \_ ромб

Переход ромба открывает новый образ в ромбе.

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
<td>Координата по оси X относительно видеокадра центра ромба.</td>
</tr>
<tr class="even">
<td>Центр по оси Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Координата по оси Y относительно видеокадра центра ромба.</td>
</tr>
<tr class="odd">
<td>Ширина</td>
<td><strong>fEffectPara2</strong></td>
<td>Ширина ромба в пикселях.</td>
</tr>
<tr class="even">
<td>Высота</td>
<td><strong>fEffectPara3</strong></td>
<td>Высота ромба в пикселях.</td>
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
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





