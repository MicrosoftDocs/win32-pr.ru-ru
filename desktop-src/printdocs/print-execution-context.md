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
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264447"
---
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="d32ec-103">\_ \_ Перечисление контекста выполнения печати</span><span class="sxs-lookup"><span data-stu-id="d32ec-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="d32ec-104">Представляет контекст выполнения при вызове [**жетпринтексекутиондата**](getprintexecutiondata.md) .</span><span class="sxs-lookup"><span data-stu-id="d32ec-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d32ec-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="d32ec-106">Константы</span><span class="sxs-lookup"><span data-stu-id="d32ec-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d32ec-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_ \_ приложение контекста выполнения \_ печати**</span><span class="sxs-lookup"><span data-stu-id="d32ec-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="d32ec-108">Вызывающий объект выполняется в приложении.</span><span class="sxs-lookup"><span data-stu-id="d32ec-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="d32ec-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ Служба диспетчера очереди для выполнения \_ печати**</span><span class="sxs-lookup"><span data-stu-id="d32ec-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="d32ec-110">Вызывающий объект выполняется в службе диспетчера очереди печати (spoolsv.exe).</span><span class="sxs-lookup"><span data-stu-id="d32ec-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="d32ec-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ узел изоляции диспетчера очереди печати контекста выполнения \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d32ec-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="d32ec-112">Вызывающий объект выполняется на узле изоляции печати (PrintIsolationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="d32ec-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="d32ec-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_ \_ \_ конвейер фильтра контекста выполнения \_ печати**</span><span class="sxs-lookup"><span data-stu-id="d32ec-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="d32ec-114">Вызывающий объект выполняется в конвейере фильтра печати (printfilterpipelinesvc.exe)</span><span class="sxs-lookup"><span data-stu-id="d32ec-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="d32ec-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**\_Контекст выполнения \_ печати \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="d32ec-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="d32ec-116">Вызывающий объект выполняется в splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="d32ec-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d32ec-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d32ec-117">Requirements</span></span>



| <span data-ttu-id="d32ec-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d32ec-118">Requirement</span></span> | <span data-ttu-id="d32ec-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d32ec-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32ec-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d32ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d32ec-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d32ec-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="d32ec-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d32ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d32ec-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d32ec-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d32ec-124">Header</span><span class="sxs-lookup"><span data-stu-id="d32ec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d32ec-125"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d32ec-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d32ec-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d32ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d32ec-127">**жетпринтексекутиондата**</span><span class="sxs-lookup"><span data-stu-id="d32ec-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="d32ec-128">**Печать \_ \_ данных выполнения**</span><span class="sxs-lookup"><span data-stu-id="d32ec-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




