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
ms.openlocfilehash: cbb6c5b19ed6116c59642e8dc5c0aa8eabf4800b066904f2132c7d182f2b7bbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070634"
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

### <a name="properties"></a>Элемент Property

Интерфейс **IEventSubscription3** имеет следующие свойства.



| Свойство                                                                                  | Тип доступа           | Описание                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**евентклассаппликатионид**](ieventsubscription3-eventclassapplicationid.md)<br/> | Чтение/запись<br/> | Идентификатор GUID приложения для объекта класса событий.<br/> |
| [**евенткласспартитионид**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Чтение/запись<br/> | Идентификатор GUID раздела объекта класса событий.<br/>   |
| [**субскрибераппликатионид**](ieventsubscription3-subscriberapplicationid.md)<br/> | Чтение/запись<br/> | Идентификатор GUID приложения подписчика.<br/>         |
| [**субскриберпартитионид**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Чтение/запись<br/> | Идентификатор GUID раздела подписчика.<br/>           |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




