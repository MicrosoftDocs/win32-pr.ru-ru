---
title: Структура ORPC_INIT_ARGS
description: '\_ \_ Структура args ОРПК init содержит сведения, используемые для инициализации удаленной отладки с помощью интерфейса иорпкдебугнотифи.'
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- ORPC_INIT_ARGS структуры COM
- COM LPORPC_INIT_ARGS указателя структуры
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135490"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="dace1-105">ОРПК \_ init \_ args, структура</span><span class="sxs-lookup"><span data-stu-id="dace1-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="dace1-106">Структура **\_ \_ args ОРПК init** содержит сведения, используемые для инициализации удаленной отладки с помощью интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="dace1-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dace1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dace1-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="dace1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dace1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dace1-109">**лпинтфорпкдебуг**</span><span class="sxs-lookup"><span data-stu-id="dace1-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="dace1-110">Указатель на интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) для использования в внутрипроцессного отладчиках.</span><span class="sxs-lookup"><span data-stu-id="dace1-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="dace1-111">Если отладчик не находится в процессе или является системой Macintosh, это поле должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dace1-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dace1-112">**пвпсн**</span><span class="sxs-lookup"><span data-stu-id="dace1-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="dace1-113">Указатель на серийный номер процесса отлаживаемого процесса в системе Macintosh.</span><span class="sxs-lookup"><span data-stu-id="dace1-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="dace1-114">Если отлаживаемый объект не является системой Macintosh, это поле должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dace1-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dace1-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="dace1-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="dace1-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dace1-116">Reserved.</span></span> <span data-ttu-id="dace1-117">Должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="dace1-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="dace1-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="dace1-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="dace1-119">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dace1-119">Reserved.</span></span> <span data-ttu-id="dace1-120">Должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="dace1-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dace1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dace1-121">Requirements</span></span>



| <span data-ttu-id="dace1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dace1-122">Requirement</span></span> | <span data-ttu-id="dace1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dace1-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="dace1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dace1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dace1-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dace1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="dace1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dace1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dace1-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dace1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dace1-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dace1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dace1-129"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="dace1-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dace1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dace1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dace1-131">**ОРПК \_ dbg \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="dace1-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="dace1-132">**\_БУФЕР ОРПК dbg \_**</span><span class="sxs-lookup"><span data-stu-id="dace1-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="dace1-133">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="dace1-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="dace1-134">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="dace1-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





