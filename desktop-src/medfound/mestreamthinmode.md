---
description: Вызывается потоком мультимедиа при запуске или при остановке потока. Дополнительные сведения об сужении см. в разделе сведения об управлении скоростью.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Событие Местреамсинмоде (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701895"
---
# <a name="mestreamthinmode-event"></a>Событие Местреамсинмоде

Вызывается потоком мультимедиа при запуске или при остановке потока. Дополнительные сведения об *сужении* см. в разделе [сведения об управлении скоростью](about-rate-control.md).

Это событие можно отправить в ответ на метод [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) или метод [**Имфкуалитядвисе:: сетдропмоде**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL.<br/></td>
<td>Указывает, началось ли тонкое начало или прекращение.<br/>
<ul>
<li>VARIANT_TRUE: образцы, доставленные после этого события, будут тоньше.</li>
<li>VARIANT_FALSE: образцы, доставленные после этого события, не будут тоньше.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




