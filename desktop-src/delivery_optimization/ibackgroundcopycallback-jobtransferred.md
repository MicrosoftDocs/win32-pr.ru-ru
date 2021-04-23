---
title: Метод Ибаккграундкопикаллбакк Жобтрансферред (Deliveryoptimization. h)
description: Оптимизация доставки (DO) вызывает реализацию метода Жобтрансферред, когда все файлы в задании были успешно переданы.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Метод Жобтрансферред
- Метод Жобтрансферред, интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, метод Жобтрансферред
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135747"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="341b2-106">Метод Ибаккграундкопикаллбакк:: Жобтрансферред</span><span class="sxs-lookup"><span data-stu-id="341b2-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="341b2-107">Оптимизация доставки (DO) вызывает реализацию метода **жобтрансферред** , когда все файлы в задании были успешно переданы.</span><span class="sxs-lookup"><span data-stu-id="341b2-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="341b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="341b2-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="341b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="341b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341b2-110">*пжоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="341b2-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341b2-111">Содержит сведения, связанные с заданиями, такие как время завершения задания, число переданных байтов и число переданных файлов.</span><span class="sxs-lookup"><span data-stu-id="341b2-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="341b2-112">Не освобождайте *пжоб*; Выпускайте интерфейс, когда метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="341b2-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341b2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="341b2-113">Return value</span></span>

<span data-ttu-id="341b2-114">Этот метод должен возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="341b2-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="341b2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="341b2-115">Remarks</span></span>

<span data-ttu-id="341b2-116">Как правило, ваша реализация должна вызвать метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) , чтобы подтвердить, что файлы успешно переданы.</span><span class="sxs-lookup"><span data-stu-id="341b2-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="341b2-117">Загружаемые файлы и файл ответов недоступны на клиенте до тех пор, пока не будет вызван **полный** метод.</span><span class="sxs-lookup"><span data-stu-id="341b2-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="341b2-118">Если не вызвать метод [**Complete**](ibackgroundcopyjob-complete.md) или метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) отменяет задание по истечении 30 дней и удаляет незавершенные файлы.</span><span class="sxs-lookup"><span data-stu-id="341b2-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="341b2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="341b2-119">Requirements</span></span>



| <span data-ttu-id="341b2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="341b2-120">Requirement</span></span> | <span data-ttu-id="341b2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="341b2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="341b2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="341b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="341b2-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="341b2-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="341b2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="341b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="341b2-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="341b2-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="341b2-126">Header</span><span class="sxs-lookup"><span data-stu-id="341b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="341b2-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="341b2-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="341b2-128">IDL</span><span class="sxs-lookup"><span data-stu-id="341b2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="341b2-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="341b2-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="341b2-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="341b2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="341b2-131"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="341b2-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="341b2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="341b2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="341b2-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="341b2-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="341b2-134">IID</span><span class="sxs-lookup"><span data-stu-id="341b2-134">IID</span></span><br/>                      | <span data-ttu-id="341b2-135">IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="341b2-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="341b2-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="341b2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341b2-137">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="341b2-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="341b2-138">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="341b2-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="341b2-139">**Использованием метода ibackgroundcopyjob:: Complete**</span><span class="sxs-lookup"><span data-stu-id="341b2-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="341b2-140">**Использованием метода ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="341b2-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





