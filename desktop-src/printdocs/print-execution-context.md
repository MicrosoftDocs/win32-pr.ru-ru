---
description: Представляет контекст выполнения при вызове Жетпринтексекутиондата.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Перечисление PRINT_EXECUTION_CONTEXT (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 78e4afb29b75c0a73799302ddb76e270b18ca2c38cb6325b59ebae5041d5f99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033962"
---
# <a name="print_execution_context-enumeration"></a>\_ \_ Перечисление контекста выполнения печати

Представляет контекст выполнения при вызове [**жетпринтексекутиондата**](getprintexecutiondata.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_ \_ приложение контекста выполнения \_ печати**
</dt> <dd>

Вызывающий объект выполняется в приложении.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ Служба диспетчера очереди для выполнения \_ печати**
</dt> <dd>

Вызывающий объект выполняется в службе диспетчера очереди печати (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ узел изоляции диспетчера очереди печати контекста выполнения \_ \_**
</dt> <dd>

Вызывающий объект выполняется на узле изоляции печати (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_ \_ \_ конвейер фильтра контекста выполнения \_ печати**
</dt> <dd>

Вызывающий объект выполняется в конвейере фильтра печати (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**\_Контекст выполнения \_ печати \_ WOW64**
</dt> <dd>

Вызывающий объект выполняется в splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**жетпринтексекутиондата**](getprintexecutiondata.md)
</dt> <dt>

[**Печать \_ \_ данных выполнения**](print-execution-data.md)
</dt> </dl>

 

 




