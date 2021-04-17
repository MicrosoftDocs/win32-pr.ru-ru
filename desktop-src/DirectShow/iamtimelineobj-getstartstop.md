---
description: Метод Жетстартстоп извлекает значения времени начала и окончания объекта относительно родителя объекта.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Метод Иамтимелинеобж:: Жетстартстоп (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685396"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="3b836-103">Метод Иамтимелинеобж:: Жетстартстоп</span><span class="sxs-lookup"><span data-stu-id="3b836-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="3b836-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3b836-104">\[Deprecated.</span></span> <span data-ttu-id="3b836-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b836-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b836-106">`GetStartStop`Метод получает значения времени начала и окончания объекта относительно родителя объекта.</span><span class="sxs-lookup"><span data-stu-id="3b836-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b836-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b836-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="3b836-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b836-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b836-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="3b836-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3b836-110">Получает время начала (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="3b836-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3b836-111">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="3b836-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="3b836-112">Получает время окончания в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="3b836-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b836-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b836-113">Return value</span></span>

<span data-ttu-id="3b836-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b836-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b836-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b836-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b836-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b836-116">Remarks</span></span>

<span data-ttu-id="3b836-117">Композиции, группы и дорожки всегда имеют время начала 0.</span><span class="sxs-lookup"><span data-stu-id="3b836-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="3b836-118">Во время подготовки к просмотру DES округляет время начала и окончания объекта до ближайшей границы фрейма.</span><span class="sxs-lookup"><span data-stu-id="3b836-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="3b836-119">Однако DES не перезаписывает время объекта.</span><span class="sxs-lookup"><span data-stu-id="3b836-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="3b836-120">При изменении частоты кадров группы округленные значения всегда вычисляются исходя из исходного времени.</span><span class="sxs-lookup"><span data-stu-id="3b836-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="3b836-121">Для получения дополнительных сведений о [времени в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="3b836-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="3b836-122">Чтобы определить время начала и окончания в готовом к просмотре проекте, передайте значения, возвращаемые методом, в `GetStartStop` метод [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md) .</span><span class="sxs-lookup"><span data-stu-id="3b836-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="3b836-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="3b836-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b836-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b836-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b836-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3b836-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b836-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3b836-126">Requirements</span></span>



| <span data-ttu-id="3b836-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3b836-127">Requirement</span></span> | <span data-ttu-id="3b836-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3b836-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b836-129">Header</span><span class="sxs-lookup"><span data-stu-id="3b836-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3b836-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b836-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b836-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b836-131">Library</span></span><br/> | <dl> <span data-ttu-id="3b836-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b836-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b836-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b836-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b836-134">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="3b836-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="3b836-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="3b836-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




