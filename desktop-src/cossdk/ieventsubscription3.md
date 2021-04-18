---
description: Хранит и извлекает сведения о подписках на события. Этот интерфейс расширяет интерфейс IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Интерфейс IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701279"
---
# <a name="ieventsubscription3-interface"></a>Интерфейс IEventSubscription3

Хранит и извлекает сведения о подписках на события. Этот интерфейс расширяет интерфейс [**IEventSubscription2**](ieventsubscription2.md) .

## <a name="when-to-implement"></a>Когда следует реализовывать

Реализовывать интерфейс **IEventSubscription3** не требуется. Предоставляемый системой класс объектов событий (CLSID \_ цевентсубскриптион) реализует **IEventSubscription3**.

## <a name="when-to-use"></a>Назначение

Система [событий COM+](com--events.md) использует этот интерфейс для получения сведений об отдельных подписках.

## <a name="members"></a>Элементы

Интерфейс **IEventSubscription3** наследует от **IEventSubscription2**. **IEventSubscription3** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IEventSubscription3** имеет следующие свойства.



| Свойство                                                                                  | Тип доступа           | Описание                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**евентклассаппликатионид**](ieventsubscription3-eventclassapplicationid.md)<br/> | Чтение/запись<br/> | Идентификатор GUID приложения для объекта класса событий.<br/> |
| [**евенткласспартитионид**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Чтение/запись<br/> | Идентификатор GUID раздела объекта класса событий.<br/>   |
| [**субскрибераппликатионид**](ieventsubscription3-subscriberapplicationid.md)<br/> | Чтение/запись<br/> | Идентификатор GUID приложения подписчика.<br/>         |
| [**субскриберпартитионид**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Чтение/запись<br/> | Идентификатор GUID раздела подписчика.<br/>           |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




