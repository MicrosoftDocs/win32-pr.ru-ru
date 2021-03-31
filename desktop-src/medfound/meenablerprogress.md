---
description: Сообщает о ходе выполнения объекта включения содержимого. Объекты, которые предоставляют интерфейс Имфконтентенаблер, могут вызвать это событие, чтобы уведомить приложение о ходе выполнения действий созидателями содержимого.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Событие Минаблерпрогресс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263650"
---
# <a name="meenablerprogress-event"></a>Событие Минаблерпрогресс

Сообщает о ходе выполнения объекта включения содержимого. Объекты, которые предоставляют интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) , могут вызвать это событие, чтобы уведомить приложение о ходе выполнения действий программы.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE               | Описание                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | Строка расширенных символов, описывающая ход выполнения.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Чтобы получить это событие, запросите интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Затем вызовите [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), как описано в разделе [генераторы событий мультимедиа](media-event-generators.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Генераторы событий мультимедиа](media-event-generators.md)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




