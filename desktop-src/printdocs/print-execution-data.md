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
# <a name="print_execution_data-structure"></a><span data-ttu-id="1a228-103">\_ \_ Структура данных выполнения печати</span><span class="sxs-lookup"><span data-stu-id="1a228-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="1a228-104">Содержит контекст выполнения драйвера принтера, который вызывает [**жетпринтексекутиондата**](getprintexecutiondata.md).</span><span class="sxs-lookup"><span data-stu-id="1a228-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a228-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a228-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="1a228-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1a228-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1a228-107">**context**</span><span class="sxs-lookup"><span data-stu-id="1a228-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="1a228-108">Значение [**\_ \_ контекста выполнения печати**](print-execution-context.md) , представляющее текущий контекст выполнения драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="1a228-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1a228-109">**клиентапппид**</span><span class="sxs-lookup"><span data-stu-id="1a228-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="1a228-110">Если значение **context** является **\_ контекстом выполнения печати \_ \_ WOW64**, **клиентапппид** определяет клиентское приложение, от имени которого splwow64.exe процесс загрузил драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="1a228-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="1a228-111">Если значение **context** не является **\_ контекстом выполнения вывода \_ \_ WOW64**, **клиентапппид** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="1a228-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a228-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1a228-112">Requirements</span></span>



| <span data-ttu-id="1a228-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1a228-113">Requirement</span></span> | <span data-ttu-id="1a228-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1a228-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a228-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a228-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1a228-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1a228-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="1a228-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a228-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1a228-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a228-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1a228-119">Header</span><span class="sxs-lookup"><span data-stu-id="1a228-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a228-120"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a228-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a228-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a228-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a228-122">**жетпринтексекутиондата**</span><span class="sxs-lookup"><span data-stu-id="1a228-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="1a228-123">**\_контекст выполнения \_ печати**</span><span class="sxs-lookup"><span data-stu-id="1a228-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




