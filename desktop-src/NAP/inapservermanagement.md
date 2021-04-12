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
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136210"
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
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Напсерверманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсерверманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы NAP](nap-interfaces.md)
</dt> <dt>

[Справочник по NAP](nap-reference.md)
</dt> </dl>

 

