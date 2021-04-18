---
description: Метод Фиксмедиатимес округляет указанные значения времени до ближайшей границы фрейма, как определено частотой выходного кадра. Как правило, приложениям не требуется вызывать этот метод.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Метод Иамтимелинесрк:: Фиксмедиатимес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685083"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="f3a73-104">Метод Иамтимелинесрк:: Фиксмедиатимес</span><span class="sxs-lookup"><span data-stu-id="f3a73-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="f3a73-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f3a73-105">\[Deprecated.</span></span> <span data-ttu-id="f3a73-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3a73-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f3a73-107">`FixMediaTimes`Метод округляет указанные значения времени до ближайшей границы фрейма, как определено частотой выходного кадра.</span><span class="sxs-lookup"><span data-stu-id="f3a73-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="f3a73-108">Как правило, приложениям не требуется вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="f3a73-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a73-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3a73-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="f3a73-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3a73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a73-111">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="f3a73-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a73-112">Указатель на переменную, которая содержит время начала (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="f3a73-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="f3a73-113">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="f3a73-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="f3a73-114">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="f3a73-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a73-115">Указатель на переменную, которая содержит время окончания в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="f3a73-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="f3a73-116">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="f3a73-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a73-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3a73-117">Return value</span></span>

<span data-ttu-id="f3a73-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f3a73-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3a73-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3a73-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a73-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3a73-120">Remarks</span></span>

<span data-ttu-id="f3a73-121">Этот метод аналогичен методу [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md) , но сохраняет исходное соотношение времени и времени работы носителя.</span><span class="sxs-lookup"><span data-stu-id="f3a73-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="f3a73-122">Простое округление времени до ближайшей границы фрейма может привести к искажению этого соотношения.</span><span class="sxs-lookup"><span data-stu-id="f3a73-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="f3a73-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f3a73-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f3a73-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f3a73-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f3a73-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f3a73-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3a73-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f3a73-126">Requirements</span></span>



| <span data-ttu-id="f3a73-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f3a73-127">Requirement</span></span> | <span data-ttu-id="f3a73-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f3a73-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a73-129">Header</span><span class="sxs-lookup"><span data-stu-id="f3a73-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f3a73-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a73-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f3a73-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3a73-131">Library</span></span><br/> | <dl> <span data-ttu-id="f3a73-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3a73-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a73-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3a73-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a73-134">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="f3a73-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f3a73-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f3a73-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




