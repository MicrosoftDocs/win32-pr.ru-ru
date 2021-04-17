---
description: Метод Втраккинсбефоре вставляет виртуальную запись в композицию с указанным приоритетом.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Метод Иамтимелинекомп:: Втраккинсбефоре (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679785"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="67b86-103">Метод Иамтимелинекомп:: Втраккинсбефоре</span><span class="sxs-lookup"><span data-stu-id="67b86-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="67b86-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="67b86-104">\[Deprecated.</span></span> <span data-ttu-id="67b86-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67b86-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67b86-106">`VTrackInsBefore`Метод вставляет виртуальную запись в композицию с указанным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="67b86-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b86-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67b86-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="67b86-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="67b86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b86-109">*пвиртуалтракк*</span><span class="sxs-lookup"><span data-stu-id="67b86-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="67b86-110">Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) виртуальной записи.</span><span class="sxs-lookup"><span data-stu-id="67b86-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="67b86-111">*Приоритет*</span><span class="sxs-lookup"><span data-stu-id="67b86-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="67b86-112">Приоритет вставки виртуальной записи или – 1, чтобы вставить виртуальную дорожку в конец списка приоритетов.</span><span class="sxs-lookup"><span data-stu-id="67b86-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="67b86-113">Список приоритетов определяет, какие клипы видимы.</span><span class="sxs-lookup"><span data-stu-id="67b86-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="67b86-114">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="67b86-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b86-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67b86-115">Return value</span></span>

<span data-ttu-id="67b86-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="67b86-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="67b86-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="67b86-117">Return code</span></span>                                                                                   | <span data-ttu-id="67b86-118">Описание</span><span class="sxs-lookup"><span data-stu-id="67b86-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="67b86-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="67b86-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="67b86-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="67b86-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="67b86-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="67b86-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="67b86-122">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="67b86-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="67b86-123"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="67b86-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="67b86-124">Объект не является виртуальной дорожкой.</span><span class="sxs-lookup"><span data-stu-id="67b86-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67b86-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67b86-125">Remarks</span></span>

<span data-ttu-id="67b86-126">Каждая виртуальная дорожка в составе имеет уникальный уровень приоритета.</span><span class="sxs-lookup"><span data-stu-id="67b86-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="67b86-127">Уровни приоритета находятся в диапазоне от 0 до *n* – 1, где *n* — число виртуальных дорожек в композиции.</span><span class="sxs-lookup"><span data-stu-id="67b86-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="67b86-128">Для видеогрупп виртуальная дорожка скрывает все виртуальные дорожки с более низким уровнем приоритета, за исключением тех мест, где дорожка пуста или содержит переход.</span><span class="sxs-lookup"><span data-stu-id="67b86-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="67b86-129">Виртуальные дорожки можно рассматривать как слои в окончательной композиции.</span><span class="sxs-lookup"><span data-stu-id="67b86-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="67b86-130">Транспортер 1 размещается поверх записи 0, а на дорожке 2 — на уровне Track 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="67b86-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="67b86-131">Если для параметра *Priority* задано значение-1, виртуальная дорожка вставляется в конец списка с более высоким значением приоритета, чем в существующих дорожках.</span><span class="sxs-lookup"><span data-stu-id="67b86-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="67b86-132">Если указать значение приоритета, которое уже существует в композиции, каждая запись с равным или более высоким приоритетом перемещается на один уровень приоритета.</span><span class="sxs-lookup"><span data-stu-id="67b86-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="67b86-133">**Пример**: Track A имеет приоритет 0, а для Track B — приоритет 1.</span><span class="sxs-lookup"><span data-stu-id="67b86-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="67b86-134">Если элемент Track C вставляется с приоритетом 0, трассировка переходит к приоритету 1, а Track B переходит к приоритету 2.</span><span class="sxs-lookup"><span data-stu-id="67b86-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="67b86-135">Если заданный приоритет больше текущего числа дорожек в композиции, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="67b86-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="67b86-136">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="67b86-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="67b86-137">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="67b86-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67b86-138">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="67b86-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67b86-139">Требования</span><span class="sxs-lookup"><span data-stu-id="67b86-139">Requirements</span></span>



| <span data-ttu-id="67b86-140">Требование</span><span class="sxs-lookup"><span data-stu-id="67b86-140">Requirement</span></span> | <span data-ttu-id="67b86-141">Значение</span><span class="sxs-lookup"><span data-stu-id="67b86-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67b86-142">Header</span><span class="sxs-lookup"><span data-stu-id="67b86-142">Header</span></span><br/>  | <dl> <span data-ttu-id="67b86-143"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="67b86-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="67b86-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="67b86-144">Library</span></span><br/> | <dl> <span data-ttu-id="67b86-145"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67b86-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b86-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67b86-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b86-147">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="67b86-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="67b86-148">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="67b86-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




