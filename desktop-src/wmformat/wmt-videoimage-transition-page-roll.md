---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Вмсдкидл. h)
description: Переход на страницу преобразует старое изображение с помощью отражения страницы и раскрывает новый рисунок под ним.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648009"
---
# <a name="wmt_videoimage_transition_page_roll"></a>ВМТ \_ видеоимаже \_ Переход \_ на \_ пробную страницу

Переход на страницу преобразует старое изображение с помощью отражения страницы и раскрывает новый рисунок под ним.

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
<td>Радиус.</td>
<td><strong>fEffectPara0</strong></td>
<td>Радиус рулона на странице.</td>
</tr>
<tr class="even">
<td>расстояние;</td>
<td><strong>fEffectPara1</strong></td>
<td>Объем нового изображения, отображаемого в пикселях в виде постраничного развертывания.</td>
</tr>
<tr class="odd">
<td>Направление</td>
<td><strong>fEffectPara2</strong></td>
<td>Угол или сторона видеокадра, из которого поступает страница. Задайте одно из следующих значений:<br/>
<ul>
<li>0 слева</li>
<li>1-правая сторона</li>
<li>2 — снизу</li>
<li>3 — сверху</li>
<li>4. левый нижний угол</li>
<li>5-нижний правый угол</li>
<li>6-верхний левый угол</li>
<li>7-верхний правый угол</li>
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

 

 





