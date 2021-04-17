---
title: Перечисление BG_JOB_STATE (Deliveryoptimization. h)
description: Перечисление BG_JOB_STATE определяет константные значения для различных состояний задания.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Перечисление BG_JOB_STATE
- Перечисление BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710456"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="a604a-105">Перечисление BG_JOB_STATE</span><span class="sxs-lookup"><span data-stu-id="a604a-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="a604a-106">Перечисление **BG_JOB_STATE** определяет константные значения для различных состояний задания.</span><span class="sxs-lookup"><span data-stu-id="a604a-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="a604a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a604a-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="a604a-108">Константы</span><span class="sxs-lookup"><span data-stu-id="a604a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a604a-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="a604a-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-110">Указывает, что задание находится в очереди и ожидает запуска.</span><span class="sxs-lookup"><span data-stu-id="a604a-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="a604a-111">Если пользователь выходит из системы во время передачи задания, задание переходит в состояние очереди.</span><span class="sxs-lookup"><span data-stu-id="a604a-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="a604a-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a604a-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="a604a-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-115">Указывает, что передает данные для задания.</span><span class="sxs-lookup"><span data-stu-id="a604a-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="a604a-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-117">Указывает, что задание приостановлено (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="a604a-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="a604a-118">Чтобы приостановить задание, вызовите метод [**использованием метода ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) .</span><span class="sxs-lookup"><span data-stu-id="a604a-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="a604a-119">Задание остается приостановленным до тех пор, пока не будет вызван метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md), [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)или [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="a604a-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="a604a-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-121">Указывает, что произошла неустранимая ошибка (службе не удается переместить файл).</span><span class="sxs-lookup"><span data-stu-id="a604a-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="a604a-122">Если ошибку, например ошибку отказа в доступе, можно исправить, вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) после устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="a604a-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="a604a-123">Однако если ошибку невозможно исправить, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) , чтобы отменить задание, или вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) , чтобы принять часть задания загрузки, которая успешно прошла передачу.</span><span class="sxs-lookup"><span data-stu-id="a604a-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="a604a-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-125">Указывает, что произошла устранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a604a-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="a604a-126">Будут повторены задания в состоянии временной ошибки на основе внутренней конфигурации повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="a604a-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="a604a-127">Состояние задания меняется на **BG_JOB_STATE_ERROR** , если задание не выполняется (см. раздел [**использованием метода ibackgroundcopyjob:: сетнопрогресстимеаут**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span><span class="sxs-lookup"><span data-stu-id="a604a-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a604a-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="a604a-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-129">Указывает, что задание успешно обработано.</span><span class="sxs-lookup"><span data-stu-id="a604a-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="a604a-130">Чтобы подтвердить завершение задания и предоставить доступ к файлам клиенту, необходимо вызвать метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="a604a-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="a604a-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-132">Указывает, что вы вызвали метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) , чтобы подтвердить успешное завершение задания.</span><span class="sxs-lookup"><span data-stu-id="a604a-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="a604a-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="a604a-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="a604a-134">Указывает, что вы вызвали метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) для отмены задания (удалите задание из очереди на перемещение).</span><span class="sxs-lookup"><span data-stu-id="a604a-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a604a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a604a-135">Requirements</span></span>



| <span data-ttu-id="a604a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a604a-136">Requirement</span></span> | <span data-ttu-id="a604a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a604a-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a604a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a604a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a604a-139">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a604a-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a604a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a604a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a604a-141">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a604a-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a604a-142">Header</span><span class="sxs-lookup"><span data-stu-id="a604a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a604a-143"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a604a-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a604a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a604a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a604a-145">**Использованием метода ibackgroundcopyjob:: State**</span><span class="sxs-lookup"><span data-stu-id="a604a-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





