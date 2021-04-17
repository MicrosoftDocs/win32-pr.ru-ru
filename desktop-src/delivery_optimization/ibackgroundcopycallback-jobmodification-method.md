---
title: Метод Ибаккграундкопикаллбакк Жобмодификатион (Deliveryoptimization. h)
description: Оптимизация доставки (DO) вызывает реализацию метода Жобмодификатион, когда задание было изменено.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Метод Жобмодификатион
- Метод Жобмодификатион, интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, метод Жобмодификатион
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710482"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="76372-106">Метод Ибаккграундкопикаллбакк:: Жобмодификатион</span><span class="sxs-lookup"><span data-stu-id="76372-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="76372-107">Оптимизация доставки (DO) вызывает реализацию метода [**жобмодификатион**](https://www.bing.com/search?q=**JobModification**) , когда задание было изменено.</span><span class="sxs-lookup"><span data-stu-id="76372-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="76372-108">Служба создает это событие, когда передаются байты, в задание добавляются файлы, свойства были изменены или изменилось состояние задания.</span><span class="sxs-lookup"><span data-stu-id="76372-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="76372-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76372-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="76372-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="76372-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76372-111">*пжоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76372-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76372-112">Содержит методы для доступа к сведениям о свойстве, ходе выполнения и состоянии задания.</span><span class="sxs-lookup"><span data-stu-id="76372-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="76372-113">Не освобождайте *пжоб*; Выпускайте интерфейс, когда метод [**жобмодификатион**](https://www.bing.com/search?q=**JobModification**) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76372-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="76372-114">*двресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76372-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76372-115">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="76372-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76372-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76372-116">Return value</span></span>

<span data-ttu-id="76372-117">Этот метод должен возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="76372-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="76372-118">Требования</span><span class="sxs-lookup"><span data-stu-id="76372-118">Requirements</span></span>



| <span data-ttu-id="76372-119">Требование</span><span class="sxs-lookup"><span data-stu-id="76372-119">Requirement</span></span> | <span data-ttu-id="76372-120">Значение</span><span class="sxs-lookup"><span data-stu-id="76372-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76372-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76372-121">Minimum supported client</span></span><br/> | <span data-ttu-id="76372-122">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="76372-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="76372-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76372-123">Minimum supported server</span></span><br/> | <span data-ttu-id="76372-124">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="76372-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="76372-125">Header</span><span class="sxs-lookup"><span data-stu-id="76372-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="76372-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="76372-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="76372-127">IDL</span><span class="sxs-lookup"><span data-stu-id="76372-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76372-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76372-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="76372-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76372-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="76372-130"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76372-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="76372-131">DLL</span><span class="sxs-lookup"><span data-stu-id="76372-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76372-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76372-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="76372-133">IID</span><span class="sxs-lookup"><span data-stu-id="76372-133">IID</span></span><br/>                      | <span data-ttu-id="76372-134">IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="76372-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="76372-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76372-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76372-136">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="76372-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="76372-137">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="76372-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





