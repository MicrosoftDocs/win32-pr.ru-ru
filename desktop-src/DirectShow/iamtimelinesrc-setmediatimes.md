---
description: Метод Сетмедиатимес задает время начала и окончания воспроизведения носителя.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Метод Иамтимелинесрк:: Сетмедиатимес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675881"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="4f92a-103">Метод Иамтимелинесрк:: Сетмедиатимес</span><span class="sxs-lookup"><span data-stu-id="4f92a-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="4f92a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4f92a-104">\[Deprecated.</span></span> <span data-ttu-id="4f92a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f92a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f92a-106">`SetMediaTimes`Метод задает время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="4f92a-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f92a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f92a-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="4f92a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f92a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f92a-109">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="4f92a-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="4f92a-110">Время начала носителя (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="4f92a-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4f92a-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="4f92a-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="4f92a-112">Время окончания носителя в единицах с 100 нс.</span><span class="sxs-lookup"><span data-stu-id="4f92a-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f92a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f92a-113">Return value</span></span>

<span data-ttu-id="4f92a-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4f92a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f92a-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f92a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f92a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f92a-116">Remarks</span></span>

<span data-ttu-id="4f92a-117">Время работы со носителями — это время начала и окончания работы относительно исходного файла носителя.</span><span class="sxs-lookup"><span data-stu-id="4f92a-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="4f92a-118">Всегда устанавливайте время носителя при добавлении источника видео или звука на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="4f92a-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="4f92a-119">В противном случае могут возникнуть проблемы отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4f92a-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="4f92a-120">Время окончания должно быть больше времени начала.</span><span class="sxs-lookup"><span data-stu-id="4f92a-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="4f92a-121">Чтобы использовать кадр по-прежнему из источника видео, задайте для параметра время окончания значение меньше времени начала, например 100 наносекунд.</span><span class="sxs-lookup"><span data-stu-id="4f92a-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="4f92a-122">Установка одного и того же значения приводит к ошибке отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4f92a-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="4f92a-123">Если длительность временной шкалы не соответствует длительности носителя, источник растягивается или сжимается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="4f92a-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="4f92a-124">Это приводит к тому, что клип будет воспроизводиться медленнее или быстрее, чем созданная скорость.</span><span class="sxs-lookup"><span data-stu-id="4f92a-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="4f92a-125">(Смещение шага произойдет в источнике звука.) Дополнительные сведения см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="4f92a-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="4f92a-126">Вы можете указать длительность исходного файла, вызвав метод [**сетмедиаленгс**](iamtimelinesrc-setmedialength.md) .</span><span class="sxs-lookup"><span data-stu-id="4f92a-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="4f92a-127">Если задать время окончания воспроизведения, превышающее длительность, DES усекает время окончания.</span><span class="sxs-lookup"><span data-stu-id="4f92a-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="4f92a-128">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4f92a-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f92a-129">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f92a-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f92a-130">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4f92a-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f92a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4f92a-131">Requirements</span></span>



| <span data-ttu-id="4f92a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4f92a-132">Requirement</span></span> | <span data-ttu-id="4f92a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4f92a-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f92a-134">Header</span><span class="sxs-lookup"><span data-stu-id="4f92a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4f92a-135"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f92a-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f92a-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f92a-136">Library</span></span><br/> | <dl> <span data-ttu-id="4f92a-137"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f92a-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f92a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f92a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f92a-139">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="4f92a-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4f92a-140">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="4f92a-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




