---
title: Перечисление Вмтаскресулт (Впккоминтерфацес. h)
description: Указывает результат задачи.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Перечисление Вмтаскресулт Virtual PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535294"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="03abd-104">Перечисление Вмтаскресулт</span><span class="sxs-lookup"><span data-stu-id="03abd-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="03abd-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="03abd-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="03abd-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="03abd-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="03abd-107">Указывает результат задачи.</span><span class="sxs-lookup"><span data-stu-id="03abd-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="03abd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03abd-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="03abd-109">Константы</span><span class="sxs-lookup"><span data-stu-id="03abd-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="03abd-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**Вмтаскресулт \_ успешно**</span><span class="sxs-lookup"><span data-stu-id="03abd-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-111">Задача выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="03abd-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**Вмтаскресулт \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="03abd-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-113">Задача отменена.</span><span class="sxs-lookup"><span data-stu-id="03abd-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**Вмтаскресулт \_ унекспектедеррор**</span><span class="sxs-lookup"><span data-stu-id="03abd-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-115">Непредвиденная ошибка в задаче.</span><span class="sxs-lookup"><span data-stu-id="03abd-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**Вмтаскресулт \_ OutOfMemoryError**</span><span class="sxs-lookup"><span data-stu-id="03abd-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-117">Недостаточно памяти для завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="03abd-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**Вмтаскресулт \_ дискрелатедеррор**</span><span class="sxs-lookup"><span data-stu-id="03abd-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-119">При записи на диск в задаче произошла ошибка (убедитесь, что на диске достаточно места).</span><span class="sxs-lookup"><span data-stu-id="03abd-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="03abd-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**Вмтаскресулт \_ инкомпатиблесаведстатиррор**</span><span class="sxs-lookup"><span data-stu-id="03abd-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-121">Не удалось восстановить виртуальную машину, так как сохраненное состояние несовместимо.</span><span class="sxs-lookup"><span data-stu-id="03abd-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**Вмтаскресулт \_ тимеаутеррор**</span><span class="sxs-lookup"><span data-stu-id="03abd-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-123">Время ожидания задачи истекло.</span><span class="sxs-lookup"><span data-stu-id="03abd-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**Вмтаскресулт \_ иллегалвалуиррор**</span><span class="sxs-lookup"><span data-stu-id="03abd-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-125">При обработке задачи было считано недопустимое значение предпочтения.</span><span class="sxs-lookup"><span data-stu-id="03abd-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**Вмтаскресулт \_ среадкрашеррор**</span><span class="sxs-lookup"><span data-stu-id="03abd-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-127">Поток, связанный с задачей, завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="03abd-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="03abd-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**Вмтаскресулт \_ шутдовнаборт**</span><span class="sxs-lookup"><span data-stu-id="03abd-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="03abd-129">Запрошенное завершение работы прервано.</span><span class="sxs-lookup"><span data-stu-id="03abd-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03abd-130">Требования</span><span class="sxs-lookup"><span data-stu-id="03abd-130">Requirements</span></span>



| <span data-ttu-id="03abd-131">Требование</span><span class="sxs-lookup"><span data-stu-id="03abd-131">Requirement</span></span> | <span data-ttu-id="03abd-132">Значение</span><span class="sxs-lookup"><span data-stu-id="03abd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="03abd-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03abd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03abd-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="03abd-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03abd-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03abd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03abd-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="03abd-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="03abd-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="03abd-137">End of client support</span></span><br/>    | <span data-ttu-id="03abd-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03abd-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="03abd-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="03abd-139">Product</span></span><br/>                  | <span data-ttu-id="03abd-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="03abd-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="03abd-141">Header</span><span class="sxs-lookup"><span data-stu-id="03abd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="03abd-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="03abd-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03abd-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03abd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03abd-144">**Ивмтаск:: result**</span><span class="sxs-lookup"><span data-stu-id="03abd-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

