---
description: Содержит контекст выполнения драйвера принтера, который вызывает Жетпринтексекутиондата.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Структура PRINT_EXECUTION_DATA (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e67b43089c275baf59295f15e84d9bf38d1a3a5ff6e2adfaf2d270b02e2ad967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447144"
---
# <a name="print_execution_data-structure"></a>\_ \_ Структура данных выполнения печати

Содержит контекст выполнения драйвера принтера, который вызывает [**жетпринтексекутиондата**](getprintexecutiondata.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**context**
</dt> <dd>

Значение [**\_ \_ контекста выполнения печати**](print-execution-context.md) , представляющее текущий контекст выполнения драйвера принтера.

</dd> <dt>

**клиентапппид**
</dt> <dd>

Если значение **context** является **\_ контекстом выполнения печати \_ \_ WOW64**, **клиентапппид** определяет клиентское приложение, от имени которого splwow64.exe процесс загрузил драйвер принтера. Если значение **context** не является **\_ контекстом выполнения вывода \_ \_ WOW64**, **клиентапппид** имеет значение 0.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетпринтексекутиондата**](getprintexecutiondata.md)
</dt> <dt>

[**\_контекст выполнения \_ печати**](print-execution-context.md)
</dt> </dl>

 

 




