---
description: Метод Жетстддев оценивает стандартное отклонение в миллисекундах между сроком выполнения каждого кадра и его фактической отрисовкой для статистики по кадрам.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Кбасевидеорендерер. Жетстддев, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657101"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="a4037-103">Кбасевидеорендерер. Жетстддев, метод</span><span class="sxs-lookup"><span data-stu-id="a4037-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="a4037-104">`GetStdDev`Метод оценивает стандартное отклонение в миллисекундах между сроком выполнения каждого кадра и его фактической отрисовкой для статистики по кадрам.</span><span class="sxs-lookup"><span data-stu-id="a4037-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4037-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4037-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="a4037-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4037-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4037-107">*нсамплес*</span><span class="sxs-lookup"><span data-stu-id="a4037-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="a4037-108">Целочисленное значение, содержащее число видеороликов, полученных модулем подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="a4037-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="a4037-109">*пиресулт*</span><span class="sxs-lookup"><span data-stu-id="a4037-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="a4037-110">Указатель на целочисленное значение, которое будет содержать стандартное отклонение.</span><span class="sxs-lookup"><span data-stu-id="a4037-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="a4037-111">*ллсумск*</span><span class="sxs-lookup"><span data-stu-id="a4037-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="a4037-112">Значение, представляющее стандартное отклонение (в миллисекундах) всех визуализированных видеороликов.</span><span class="sxs-lookup"><span data-stu-id="a4037-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="a4037-113">Чем меньше значение, тем более последовательна отрисовка.</span><span class="sxs-lookup"><span data-stu-id="a4037-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="a4037-114">*итот*</span><span class="sxs-lookup"><span data-stu-id="a4037-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="a4037-115">Значение, представляющее среднее значение в миллисекундах между отметкой времени и временем визуализации для всех визуализированных видеороликов.</span><span class="sxs-lookup"><span data-stu-id="a4037-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4037-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4037-116">Return value</span></span>

<span data-ttu-id="a4037-117">Возвращает значение "ошибка".</span><span class="sxs-lookup"><span data-stu-id="a4037-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4037-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a4037-118">Requirements</span></span>



| <span data-ttu-id="a4037-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a4037-119">Requirement</span></span> | <span data-ttu-id="a4037-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a4037-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4037-121">Header</span><span class="sxs-lookup"><span data-stu-id="a4037-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a4037-122"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4037-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4037-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4037-123">Library</span></span><br/> | <dl> <span data-ttu-id="a4037-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a4037-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4037-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4037-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4037-126">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="a4037-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




