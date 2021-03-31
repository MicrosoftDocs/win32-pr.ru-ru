---
title: Интерфейс INapSystemHealthAgentBinding2 (Напсистемхеалсажент. h)
description: SHA использует для взаимодействия с Напажент. | Интерфейс INapSystemHealthAgentBinding2 (Напсистемхеалсажент. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2 интерфейса NAP
- INapSystemHealthAgentBinding2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352795"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>Интерфейс INapSystemHealthAgentBinding2

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

**INapSystemHealthAgentBinding2** предоставляет методы, которые SHA использует для взаимодействия с напажент.

> [!Note]  
> Этот интерфейс наследует все методы [**инапсистемхеалсажентбиндинг**](inapsystemhealthagentbinding.md) и использовать вместо него.

 

## <a name="members"></a>Элементы

Интерфейс **INapSystemHealthAgentBinding2** наследует от [**инапсистемхеалсажентбиндинг**](inapsystemhealthagentbinding.md). **INapSystemHealthAgentBinding2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **INapSystemHealthAgentBinding2** содержит следующие методы.



| Метод                                                                                                                    | Описание                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2:: Жетсистемисолатионинфоекс**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Вызывается SHA для определения состояния изоляции системы и расширенного состояния изоляции.<br/> |



 

## <a name="remarks"></a>Комментарии

Все API-интерфейсы в этом интерфейсе будут возвращать **RPC \_ E \_ disconnected** , если напажент остановлен. После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Напсистемхеалсажент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсистемхеалсажент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапсистемхеалсажентбиндинг**](inapsystemhealthagentbinding.md)
</dt> <dt>

[Интерфейсы NAP](nap-interfaces.md)
</dt> <dt>

[Справочник по NAP](nap-reference.md)
</dt> </dl>

 

 





