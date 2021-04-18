---
title: Интерфейс Ибаккграундкопикаллбакк (Deliveryoptimization. h)
description: Реализуйте интерфейс Ибаккграундкопикаллбакк, чтобы получить уведомление о завершении задания, его изменении или об ошибке. Клиенты используют этот интерфейс вместо опроса состояния задания.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710481"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="633b5-106">Интерфейс Ибаккграундкопикаллбакк</span><span class="sxs-lookup"><span data-stu-id="633b5-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="633b5-107">Реализуйте интерфейс **ибаккграундкопикаллбакк** , чтобы получить уведомление о завершении задания, его изменении или об ошибке.</span><span class="sxs-lookup"><span data-stu-id="633b5-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="633b5-108">Клиенты используют этот интерфейс вместо опроса состояния задания.</span><span class="sxs-lookup"><span data-stu-id="633b5-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="633b5-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="633b5-109">Members</span></span>

<span data-ttu-id="633b5-110">Интерфейс **ибаккграундкопикаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="633b5-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="633b5-111">**Ибаккграундкопикаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="633b5-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="633b5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="633b5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="633b5-113">Методы</span><span class="sxs-lookup"><span data-stu-id="633b5-113">Methods</span></span>

<span data-ttu-id="633b5-114">Интерфейс **ибаккграундкопикаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="633b5-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="633b5-115">Метод</span><span class="sxs-lookup"><span data-stu-id="633b5-115">Method</span></span>                                                                    | <span data-ttu-id="633b5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="633b5-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="633b5-117">**жоберрор**</span><span class="sxs-lookup"><span data-stu-id="633b5-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="633b5-118">Вызывается при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="633b5-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="633b5-119">**жобмодификатион**</span><span class="sxs-lookup"><span data-stu-id="633b5-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="633b5-120">Вызывается при изменении задания.</span><span class="sxs-lookup"><span data-stu-id="633b5-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="633b5-121">**жобтрансферред**</span><span class="sxs-lookup"><span data-stu-id="633b5-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="633b5-122">Вызывается, когда все файлы в задании успешно переданы.</span><span class="sxs-lookup"><span data-stu-id="633b5-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="633b5-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="633b5-123">Remarks</span></span>

<span data-ttu-id="633b5-124">Чтобы получать уведомления, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md) , чтобы указать указатель интерфейса на реализацию **ибаккграундкопикаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="633b5-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="633b5-125">Чтобы указать, какие уведомления необходимо получать, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md) .</span><span class="sxs-lookup"><span data-stu-id="633b5-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="633b5-126">При условии, что указатель интерфейса является допустимым, будут вызываться обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="633b5-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="633b5-127">Интерфейс уведомления больше не действителен после завершения работы приложения. Не сохраняет интерфейс уведомления.</span><span class="sxs-lookup"><span data-stu-id="633b5-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="633b5-128">В результате процесс инициализации приложения должен вызвать метод [**сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md) для тех существующих заданий, для которых вы хотите получить уведомление.</span><span class="sxs-lookup"><span data-stu-id="633b5-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="633b5-129">Требования</span><span class="sxs-lookup"><span data-stu-id="633b5-129">Requirements</span></span>



| <span data-ttu-id="633b5-130">Требование</span><span class="sxs-lookup"><span data-stu-id="633b5-130">Requirement</span></span> | <span data-ttu-id="633b5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="633b5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="633b5-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="633b5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="633b5-133">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="633b5-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="633b5-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="633b5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="633b5-135">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="633b5-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="633b5-136">Header</span><span class="sxs-lookup"><span data-stu-id="633b5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="633b5-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="633b5-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="633b5-138">IDL</span><span class="sxs-lookup"><span data-stu-id="633b5-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="633b5-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="633b5-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="633b5-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="633b5-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="633b5-141"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="633b5-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="633b5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="633b5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="633b5-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="633b5-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="633b5-144">IID</span><span class="sxs-lookup"><span data-stu-id="633b5-144">IID</span></span><br/>                      | <span data-ttu-id="633b5-145">IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="633b5-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="633b5-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="633b5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633b5-147">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="633b5-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="633b5-148">**Использованием метода ibackgroundcopyjob:: Сетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="633b5-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="633b5-149">**Использованием метода ibackgroundcopyjob:: Сетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="633b5-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

