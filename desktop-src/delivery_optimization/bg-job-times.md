---
title: Структура BG_JOB_TIMES (Deliveryoptimization. h)
description: Структура BG_JOB_TIMES предоставляет штампы времени, связанные с заданием.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Структура BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801391"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="99b73-104">Структура BG_JOB_TIMES</span><span class="sxs-lookup"><span data-stu-id="99b73-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="99b73-105">Структура **BG_JOB_TIMES** предоставляет штампы времени, связанные с заданием.</span><span class="sxs-lookup"><span data-stu-id="99b73-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b73-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99b73-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="99b73-107">Члены</span><span class="sxs-lookup"><span data-stu-id="99b73-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="99b73-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="99b73-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="99b73-109">Время создания задания.</span><span class="sxs-lookup"><span data-stu-id="99b73-109">Time the job was created.</span></span> <span data-ttu-id="99b73-110">Время указывается в виде [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="99b73-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="99b73-111">**модификатионтиме**</span><span class="sxs-lookup"><span data-stu-id="99b73-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="99b73-112">Время последнего изменения задания или передачи байтов.</span><span class="sxs-lookup"><span data-stu-id="99b73-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="99b73-113">Изменение этого значения осуществляется путем добавления файлов или вызова любого из методов Set в интерфейсах [ \* *использованием метода ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="99b73-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="99b73-114">Кроме того, изменения в состоянии задания и вызов методов [_ *Suspend* \*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)и [**Complete**](ibackgroundcopyjob-complete.md) изменяют это значение.</span><span class="sxs-lookup"><span data-stu-id="99b73-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="99b73-115">Время указывается в виде [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="99b73-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="99b73-116">**трансферкомплетионтиме**</span><span class="sxs-lookup"><span data-stu-id="99b73-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="99b73-117">Время, когда задание перешло в состояние BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="99b73-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="99b73-118">Время указывается в виде [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="99b73-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99b73-119">Требования</span><span class="sxs-lookup"><span data-stu-id="99b73-119">Requirements</span></span>



| <span data-ttu-id="99b73-120">Требование</span><span class="sxs-lookup"><span data-stu-id="99b73-120">Requirement</span></span> | <span data-ttu-id="99b73-121">Значение</span><span class="sxs-lookup"><span data-stu-id="99b73-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b73-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99b73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99b73-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="99b73-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="99b73-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99b73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99b73-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="99b73-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="99b73-126">Header</span><span class="sxs-lookup"><span data-stu-id="99b73-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b73-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b73-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b73-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99b73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b73-129">**Использованием метода ibackgroundcopyjob:: навремя**</span><span class="sxs-lookup"><span data-stu-id="99b73-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

