---
description: Метод Счедулесампле переопределяет базовый класс, который выполняет основную работу, чтобы обеспечить Количество рисуемых и удаленных выборок (которые используются реализацией Икуалпроп).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Кбасевидеорендерер. Счедулесампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675001"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="140a7-103">Кбасевидеорендерер. Счедулесампле, метод</span><span class="sxs-lookup"><span data-stu-id="140a7-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="140a7-104">`ScheduleSample`Метод переопределяет базовый класс, который выполняет основную работу, чтобы обеспечить количество выводимых и удаленных выборок (которые используются реализацией [**икуалпроп**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).</span><span class="sxs-lookup"><span data-stu-id="140a7-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="140a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="140a7-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="140a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="140a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140a7-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="140a7-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="140a7-108">Указатель на пример носителя.</span><span class="sxs-lookup"><span data-stu-id="140a7-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140a7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="140a7-109">Return value</span></span>

<span data-ttu-id="140a7-110">Возвращает **значение true** , если выборка запланирована. в противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="140a7-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="140a7-111">Требования</span><span class="sxs-lookup"><span data-stu-id="140a7-111">Requirements</span></span>



| <span data-ttu-id="140a7-112">Требование</span><span class="sxs-lookup"><span data-stu-id="140a7-112">Requirement</span></span> | <span data-ttu-id="140a7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="140a7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140a7-114">Header</span><span class="sxs-lookup"><span data-stu-id="140a7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="140a7-115"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="140a7-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="140a7-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="140a7-116">Library</span></span><br/> | <dl> <span data-ttu-id="140a7-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="140a7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140a7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="140a7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140a7-119">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="140a7-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




