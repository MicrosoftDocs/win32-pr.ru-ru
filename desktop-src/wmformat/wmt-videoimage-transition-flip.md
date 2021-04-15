---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Вмсдкидл. h)
description: Переход «Перелистывание» поворачивает старое изображение на оси y через центр фрейма. Новый образ будет отображен в качестве обратной стороны старого образа.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649102"
---
# <a name="wmt_videoimage_transition_flip"></a>\_отразить \_ Переход ВМТ видеоимаже \_

Переход «Перелистывание» поворачивает старое изображение на оси y через центр фрейма. Новый образ будет отображен в качестве обратной стороны старого образа.

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
<td>Angle</td>
<td><strong>fEffectPara0</strong></td>
<td>Угол поворота (от 0,0 до 180,0 градусов).</td>
</tr>
<tr class="even">
<td>Композиция</td>
<td><strong>fEffectPara1</strong></td>
<td>Задайте одно из следующих значений:
<ul>
<li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li>
<li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Вы можете визуализировать результат этого перехода, как если бы оба изображения были связаны между собой физическими фотографиями. Переход имеет тот же результат, что и удержание двух таких фотографий в центре нижнего края и поворот их на 180 градусов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





