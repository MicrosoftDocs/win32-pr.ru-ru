---
title: Метод Ивмтаск Ваитфоркомплетион (Впккоминтерфацес. h)
description: Ожидает завершения задачи или до истечения указанного интервала времени ожидания.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Метод Ваитфоркомплетион Virtual PC
- Метод Ваитфоркомплетион Virtual PC, интерфейс Ивмтаск
- Ивмтаск интерфейс Virtual PC, метод Ваитфоркомплетион
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691894"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="6486e-106">Метод Ивмтаск:: Ваитфоркомплетион</span><span class="sxs-lookup"><span data-stu-id="6486e-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="6486e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6486e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6486e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6486e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6486e-109">Ожидает завершения задачи или до истечения указанного интервала времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="6486e-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="6486e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6486e-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="6486e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6486e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6486e-112">*время ожидания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6486e-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6486e-113">Время в миллисекундах, в течение которого этот метод будет ожидать завершения задачи перед возвратом управления вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="6486e-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="6486e-114">Значение-1 указывает, что метод будет ожидать завершения задачи без истечения времени ожидания. Другие допустимые значения времени ожидания находятся в диапазоне от 0 до 4 000 000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="6486e-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6486e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6486e-115">Return value</span></span>

<span data-ttu-id="6486e-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6486e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="6486e-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="6486e-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="6486e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6486e-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6486e-119"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6486e-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6486e-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6486e-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="6486e-121"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6486e-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="6486e-122">Недопустимый параметр *времени ожидания* .</span><span class="sxs-lookup"><span data-stu-id="6486e-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6486e-123"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6486e-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6486e-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6486e-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6486e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6486e-125">Remarks</span></span>

<span data-ttu-id="6486e-126">Метод **ваитфоркомплетион** помещает текущий поток выполнения в спящий режим до тех пор, пока не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="6486e-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="6486e-127">Указание бесконечного ожидания (timeout =-1) не рекомендуется, если не крайне важно, чтобы задача завершилась при каких-либо обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="6486e-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6486e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="6486e-128">Requirements</span></span>



| <span data-ttu-id="6486e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="6486e-129">Requirement</span></span> | <span data-ttu-id="6486e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6486e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6486e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6486e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6486e-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6486e-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6486e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6486e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6486e-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6486e-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6486e-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6486e-135">End of client support</span></span><br/>    | <span data-ttu-id="6486e-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6486e-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6486e-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="6486e-137">Product</span></span><br/>                  | <span data-ttu-id="6486e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6486e-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6486e-139">Header</span><span class="sxs-lookup"><span data-stu-id="6486e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6486e-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6486e-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6486e-141">IID</span><span class="sxs-lookup"><span data-stu-id="6486e-141">IID</span></span><br/>                      | <span data-ttu-id="6486e-142">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="6486e-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="6486e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6486e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6486e-144">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="6486e-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

