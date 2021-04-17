---
description: Хранит и извлекает сведения о подписках на события. Этот интерфейс расширяет интерфейс Иевентсубскриптион.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Интерфейс IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682366"
---
# <a name="ieventsubscription2-interface"></a>Интерфейс IEventSubscription2

Хранит и извлекает сведения о подписках на события. Этот интерфейс расширяет интерфейс [**иевентсубскриптион**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .

## <a name="when-to-implement"></a>Когда следует реализовывать

Реализовывать интерфейс **IEventSubscription2** не требуется. Предоставляемый системой класс объектов событий (CLSID \_ цевентсубскриптион) реализует **IEventSubscription2**.

## <a name="when-to-use"></a>Назначение

Система [событий COM+](com--events.md) использует этот интерфейс для получения сведений об отдельных подписках.

## <a name="members"></a>Элементы

Интерфейс **IEventSubscription2** наследует от **иевентсубскриптион**. **IEventSubscription2** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IEventSubscription2** имеет следующие свойства.



| Свойство                                                                      | Тип доступа           | Описание                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**Параметром filterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Чтение/запись<br/> | Критерии фильтра, управляющие подпиской.<br/> |
| [**субскрибермоникер**](ieventsubscription2-subscribermoniker.md)<br/> | Чтение/запись<br/> | Моникер подписчика.<br/>                       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иевентсубскриптион**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




