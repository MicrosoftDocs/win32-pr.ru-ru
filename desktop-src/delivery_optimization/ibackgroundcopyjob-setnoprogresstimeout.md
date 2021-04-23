---
title: Метод использованием метода ibackgroundcopyjob Сетнопрогресстимеаут (Deliveryoptimization. h)
description: Задает период времени, в течение которого оптимизация доставки (DO) пытается передавать файл после возникновения временной ошибки. Если происходит выполнение, таймер сбрасывается.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Метод Сетнопрогресстимеаут
- Метод Сетнопрогресстимеаут, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Сетнопрогресстимеаут
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071690"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="fb95b-107">Метод использованием метода ibackgroundcopyjob:: Сетнопрогресстимеаут</span><span class="sxs-lookup"><span data-stu-id="fb95b-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="fb95b-108">Задает период времени, в течение которого оптимизация доставки (DO) пытается передавать файл после возникновения временной ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb95b-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="fb95b-109">Если происходит выполнение, таймер сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="fb95b-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb95b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb95b-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="fb95b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb95b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb95b-112">*Ретрипериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb95b-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb95b-113">Время в секундах, которое пытается переместить файл после того, как он не был выполнен.</span><span class="sxs-lookup"><span data-stu-id="fb95b-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="fb95b-114">Период повтора по умолчанию для задания с высоким приоритетом составляет 3600 секунд (1 час), а для задания с низким приоритетом — 86400 секунд (24 часа).</span><span class="sxs-lookup"><span data-stu-id="fb95b-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb95b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb95b-115">Return value</span></span>

<span data-ttu-id="fb95b-116">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="fb95b-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="fb95b-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fb95b-117">Return code</span></span>                                                                                          | <span data-ttu-id="fb95b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fb95b-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb95b-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="fb95b-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="fb95b-120">Период повтора успешно задан.</span><span class="sxs-lookup"><span data-stu-id="fb95b-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="fb95b-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="fb95b-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="fb95b-122">Состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="fb95b-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb95b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb95b-123">Remarks</span></span>

<span data-ttu-id="fb95b-124">Если не выполняется в течение периода повтора, то состояние задания перемещается с BG_JOB_STATE_TRANSIENT_ERROR на BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="fb95b-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="fb95b-125">Если вы запрашиваете уведомление об ошибке, выполните вызов обратного вызова [**жоберрор**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="fb95b-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb95b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="fb95b-126">Requirements</span></span>



| <span data-ttu-id="fb95b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="fb95b-127">Requirement</span></span> | <span data-ttu-id="fb95b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fb95b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb95b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb95b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb95b-130">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="fb95b-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fb95b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb95b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb95b-132">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="fb95b-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fb95b-133">Header</span><span class="sxs-lookup"><span data-stu-id="fb95b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb95b-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb95b-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb95b-135">IDL</span><span class="sxs-lookup"><span data-stu-id="fb95b-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb95b-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb95b-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fb95b-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb95b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb95b-138"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb95b-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fb95b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fb95b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb95b-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb95b-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fb95b-141">IID</span><span class="sxs-lookup"><span data-stu-id="fb95b-141">IID</span></span><br/>                      | <span data-ttu-id="fb95b-142">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="fb95b-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fb95b-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb95b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb95b-144">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="fb95b-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="fb95b-145">**Использованием метода ibackgroundcopyjob:: Жетнопрогресстимеаут**</span><span class="sxs-lookup"><span data-stu-id="fb95b-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





