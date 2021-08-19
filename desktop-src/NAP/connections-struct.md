---
title: Структура подключений (Напенфорцементклиент. h)
description: Содержит сведения о списке соединений, поддерживаемых средством применения.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Структура подключений NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91e2dc404ff50c7edc3ba80a3c772ac6be762c1fe49575d8503a783e83bbef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800151"
---
# <a name="connections-structure"></a>Структура соединений

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Структура **Connections** содержит сведения о списке соединений, обслуживаемых средством применения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>Члены

<dl> <dt>

**count**
</dt> <dd>

Число активных соединений, которые в настоящее время поддерживаются принудительно в диапазоне от 0 (нуля) до [**максконнектионкаунтперенфорцер**](nap-type-constants.md).

</dd> <dt>

**подключения**
</dt> <dd>

COM-указатель на список интерфейсов [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , представляющих клиентские соединения.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по NAP](nap-reference.md)
</dt> <dt>

[Структуры NAP](nap-structures.md)
</dt> <dt>

[**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





