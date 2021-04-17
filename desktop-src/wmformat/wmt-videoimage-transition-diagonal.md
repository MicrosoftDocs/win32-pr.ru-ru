---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Вмсдкидл. h)
description: Диагональный переход показывает новый рисунок вдоль диагональной линии, порожденной в одном углу рамки.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685267"
---
# <a name="wmt_videoimage_transition_diagonal"></a>ВМТ \_ видеоимаже \_ Переход по \_ диагонали

Диагональный переход показывает новый рисунок вдоль диагональной линии, порожденной в одном углу рамки.

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
<td>Ширина диагональной секции в пикселях.</td>
</tr>
<tr class="even">
<td>Высота</td>
<td><strong>fEffectPara1</strong></td>
<td>Высота диагональной секции в пикселях.</td>
</tr>
<tr class="odd">
<td>Направление</td>
<td><strong>fEffectPara2</strong></td>
<td>Определяет угол, с которого исходит переход. Задайте один из следующих элементов:<br/>
<ul>
<li>0-верхний правый</li>
<li>1-верхний левый</li>
<li>2-вниз справа</li>
<li>3-вниз слева</li>
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
| Header<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





