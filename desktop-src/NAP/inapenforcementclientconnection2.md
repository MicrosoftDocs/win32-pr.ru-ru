---
title: Интерфейс INapEnforcementClientConnection2 (Напенфорцементклиент. h)
description: Разрешить управление клиентскими подключениями. | Интерфейс INapEnforcementClientConnection2 (Напенфорцементклиент. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2 интерфейса NAP
- INapEnforcementClientConnection2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60e91ffbc12534bb3b5a8ac22cbd13a1238ba32e09b4f56b4ab570ffd1ea8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144397"
---
# <a name="inapenforcementclientconnection2-interface"></a>Интерфейс INapEnforcementClientConnection2

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

**INapEnforcementClientConnection2** предоставляет методы, позволяющие управлять подключениями клиентов.

> [!Note]  
> Этот интерфейс наследует все методы [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) и использовать вместо него.

 

## <a name="members"></a>Элементы

Интерфейс **INapEnforcementClientConnection2** наследует от [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **INapEnforcementClientConnection2** содержит следующие методы.



| Метод                                                                                                              | Описание                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2:: Жетинсталледшвс**](inapenforcementclientconnection2-getinstalledshvs.md)     | Используется для получения идентификаторов установленных SHV для клиента.<br/>             |
| [**INapEnforcementClientConnection2:: Жетисолатионинфоекс**](inapenforcementclientconnection2-getisolationinfoex.md) | Используется для получения сведений о изоляции клиента.<br/>                 |
| [**INapEnforcementClientConnection2:: Сетинсталледшвс**](inapenforcementclientconnection2-setinstalledshvs.md)     | Используется Напажент для установки установленных идентификаторов SHV для клиента.<br/>     |
| [**INapEnforcementClientConnection2:: Сетисолатионинфоекс**](inapenforcementclientconnection2-setisolationinfoex.md) | Используется Напажент для установки сведений о изоляции клиента.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md)
</dt> <dt>

[Интерфейсы NAP](nap-interfaces.md)
</dt> <dt>

[Справочник по NAP](nap-reference.md)
</dt> </dl>

 

 





