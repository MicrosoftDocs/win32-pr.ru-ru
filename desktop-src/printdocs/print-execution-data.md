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
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265870"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетпринтексекутиондата**](getprintexecutiondata.md)
</dt> <dt>

[**\_контекст выполнения \_ печати**](print-execution-context.md)
</dt> </dl>

 

 




