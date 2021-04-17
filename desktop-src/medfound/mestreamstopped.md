---
description: 'Вызывается потоком мультимедиа, когда метод Имфмедиасаурце:: останавливаться завершается асинхронно.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Событие Местреамстоппед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702551"
---
# <a name="mestreamstopped-event"></a>Событие Местреамстоппед

Вызывается потоком мультимедиа, когда метод [**имфмедиасаурце:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) завершается асинхронно.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Каждый активный поток в презентации отправляет это событие.

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

 

 




