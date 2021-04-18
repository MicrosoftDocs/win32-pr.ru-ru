---
description: Метод Сетстартстоп задает время начала и окончания объекта относительно родителя объекта.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Метод Иамтимелинеобж:: Сетстартстоп (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689143"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="ae2e8-103">Метод Иамтимелинеобж:: Сетстартстоп</span><span class="sxs-lookup"><span data-stu-id="ae2e8-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="ae2e8-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-104">\[Deprecated.</span></span> <span data-ttu-id="ae2e8-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae2e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ae2e8-106">`SetStartStop`Метод задает время начала и окончания объекта относительно родителя объекта.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae2e8-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="ae2e8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae2e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2e8-109">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="ae2e8-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="ae2e8-110">Новое время начала, в 100-наносекундных единицах или – 1 для сохранения существующего времени начала.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="ae2e8-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="ae2e8-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="ae2e8-112">Новое время окончания, в 100-наносекундных единицах или – 1 для сохранения текущего времени окончания.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2e8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae2e8-113">Return value</span></span>

<span data-ttu-id="ae2e8-114">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="ae2e8-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ae2e8-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ae2e8-115">Return code</span></span>                                                                                  | <span data-ttu-id="ae2e8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ae2e8-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="ae2e8-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2e8-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ae2e8-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="ae2e8-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2e8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ae2e8-120">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="ae2e8-121"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2e8-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="ae2e8-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="ae2e8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae2e8-123">Remarks</span></span>

<span data-ttu-id="ae2e8-124">Отслеживание, композиции и группы не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="ae2e8-125">Для этих объектов время начала всегда равно нулю, а время окончания — на максимальное время окончания содержащихся в них объектов.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="ae2e8-126">Не задавайте перекрывающиеся значения времени на объекты источника в одной и той же дорожке. Это может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="ae2e8-127">Для исходных объектов время начала и окончания не зависит от времени начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="ae2e8-128">Изменение одной пары значений не приводит к изменению другой.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="ae2e8-129">Чтобы задать время начала и окончания воспроизведения носителя, вызовите метод [**иамтимелинесрк:: сетмедиатимес**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2e8-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="ae2e8-130">Дополнительные сведения см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="ae2e8-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="ae2e8-131">Для получения точных покадровых *выпусков* и переходов задайте параметры запуска и *окончания* для границ фрейма.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="ae2e8-132">Можно использовать метод [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md) для преобразования значения времени в ближайшую границу фрейма или использовать следующую функцию для преобразования из номера кадра в ссылочное время:</span><span class="sxs-lookup"><span data-stu-id="ae2e8-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="ae2e8-133">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae2e8-134">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae2e8-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ae2e8-135">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ae2e8-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae2e8-136">Требования</span><span class="sxs-lookup"><span data-stu-id="ae2e8-136">Requirements</span></span>



| <span data-ttu-id="ae2e8-137">Требование</span><span class="sxs-lookup"><span data-stu-id="ae2e8-137">Requirement</span></span> | <span data-ttu-id="ae2e8-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ae2e8-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2e8-139">Header</span><span class="sxs-lookup"><span data-stu-id="ae2e8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="ae2e8-140"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2e8-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ae2e8-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae2e8-141">Library</span></span><br/> | <dl> <span data-ttu-id="ae2e8-142"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2e8-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2e8-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae2e8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2e8-144">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="ae2e8-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ae2e8-145">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ae2e8-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




