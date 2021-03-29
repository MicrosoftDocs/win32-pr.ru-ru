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
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989420"
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

**соединение**
</dt> <dd>

COM-указатель на список интерфейсов [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , представляющих клиентские соединения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по NAP](nap-reference.md)
</dt> <dt>

[Структуры NAP](nap-structures.md)
</dt> <dt>

[**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





