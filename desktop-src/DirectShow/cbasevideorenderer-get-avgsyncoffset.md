---
description: Метод Get \_ авгсинкоффсет извлекает среднее значение времени в миллисекундах между временем выполнения каждого кадра и моментом его отрисовки для всех кадров с момента запуска потоковой передачи.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Метод CBaseVideoRenderer.get_AvgSyncOffset (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675215"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="2a709-103">Кбасевидеорендерер. Get \_ авгсинкоффсет, метод</span><span class="sxs-lookup"><span data-stu-id="2a709-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="2a709-104">`get_AvgSyncOffset`Метод получает среднее значение времени в миллисекундах между временем выполнения каждого кадра и временем его отрисовки для всех кадров с момента запуска потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="2a709-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a709-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a709-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="2a709-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a709-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a709-107">*пиавг*</span><span class="sxs-lookup"><span data-stu-id="2a709-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="2a709-108">Указатель на среднее значение времени, описанное ранее.</span><span class="sxs-lookup"><span data-stu-id="2a709-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a709-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a709-109">Return value</span></span>

<span data-ttu-id="2a709-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a709-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a709-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a709-111">Remarks</span></span>

<span data-ttu-id="2a709-112">Эта функция члена реализует метод [**икуалпроп:: Get \_ авгсинкоффсет**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="2a709-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a709-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2a709-113">Requirements</span></span>



| <span data-ttu-id="2a709-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2a709-114">Requirement</span></span> | <span data-ttu-id="2a709-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2a709-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a709-116">Header</span><span class="sxs-lookup"><span data-stu-id="2a709-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2a709-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a709-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2a709-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a709-118">Library</span></span><br/> | <dl> <span data-ttu-id="2a709-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2a709-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a709-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a709-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a709-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="2a709-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




