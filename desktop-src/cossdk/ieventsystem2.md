---
description: Используется службой уведомлений о системных событиях Microsoft Internet Explorer (Сенс) для доступа к хранилищу данных событий. Этот интерфейс расширяет интерфейс Иевентсистем.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Интерфейс IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6ecee3137750da9f86b61696799a3a7c6e7177beb2b92fb386712a6c90f69d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070604"
---
# <a name="ieventsystem2-interface"></a>Интерфейс IEventSystem2

Используется службой уведомлений о системных событиях Microsoft Internet Explorer (Сенс) для доступа к хранилищу данных событий. Этот интерфейс расширяет интерфейс [**иевентсистем**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .

## <a name="when-to-implement"></a>Когда следует реализовывать

Реализовывать интерфейс **IEventSystem2** не требуется. Предоставляемый системой системный объект событий (CLSID \_ цевентсистем) реализует **IEventSystem2**.

## <a name="when-to-use"></a>Назначение

При использовании Сенс можно вызывать методы **IEventSystem2** для добавления и удаления объектов из хранилища событий и получения объектов из хранилища событий.

Поскольку [**иевентпублишер**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) и объект издателя больше не поддерживаются, [**иевентобжектчанже**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) не вызывается в методе [**чанжедпублишер**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .

## <a name="members"></a>Элементы

Интерфейс **IEventSystem2** наследует от **иевентсистем**. **IEventSystem2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IEventSystem2** содержит следующие методы.



| Метод                                                                         | Описание                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | Возвращает номер версии системы событий.<br/>                      |
| [**верифитрансиентсубскриберс**](ieventsystem2-verifytransientsubscribers.md) | Проверяет существование всех временных подписчиков в хранилище данных.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иевентсистем**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

