---
description: Интерфейс Имониторевентер предоставляет методы для отправки событий и выделения и освобождения ресурсов монитора.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Интерфейс Имониторевентер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2af49529a74c23e0f4d4e77e0d2608cd44d12028d93022750fbbd3af891e2e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365492"
---
# <a name="imonitoreventer-interface"></a>Интерфейс Имониторевентер

Интерфейс **имониторевентер** предоставляет методы для отправки событий и выделения и освобождения ресурсов монитора.

## <a name="members"></a>Элементы

Интерфейс **имониторевентер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Имониторевентер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **имониторевентер** содержит следующие методы.



| Метод                                                 | Описание                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**фриевентдата**](imonitoreventer-freeeventdata.md) | Освобождает место, выделенное для данных монитора.<br/> |
| [**жетевентдата**](imonitoreventer-geteventdata.md)   | Выделяет место для данных монитора.<br/>       |
| [**сенднмевент**](imonitoreventer-sendnmevent.md)     | Отправляет события в WMI.<br/>                  |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

