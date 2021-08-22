---
title: Интерфейс Инапсерверманажемент (Напсерверманажемент. h)
description: Используются для управления сервером защиты доступа к сети.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- Инапсерверманажемент интерфейса NAP
- Инапсерверманажемент интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b324f32c542a6a300266d26ceb5981bb6e14d0feff28aa225698d6b32bbe94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012532"
---
# <a name="inapservermanagement-interface"></a>Интерфейс Инапсерверманажемент

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

**Инапсерверманажемент** предоставляет методы, используемые для управления сервером NAP.

## <a name="members"></a>Элементы

Интерфейс **инапсерверманажемент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Инапсерверманажемент** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **инапсерверманажемент** содержит следующие методы.



| Метод                                                                                                                       | Описание                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**Инапсерверманажемент:: Регистерсистемхеалсвалидатор**](inapservermanagement-registersystemhealthvalidator-method.md)     | Регистрирует SHV.<br/>                         |
| [**Инапсерверманажемент:: Сетфаилурекатегоримаппингс**](inapservermanagement-setfailurecategorymappings-method.md)           | Задает сопоставления категорий сбоев SHV.<br/> |
| [**Инапсерверманажемент:: Унрегистерсистемхеалсвалидатор**](inapservermanagement-unregistersystemhealthvalidator-method.md) | Отменяет регистрацию SHV на сервере NAP.<br/>   |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                               |
| Заголовок<br/>                   | <dl> <dt>Напсерверманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсерверманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы NAP](nap-interfaces.md)
</dt> <dt>

[Справочник по NAP](nap-reference.md)
</dt> </dl>

 

