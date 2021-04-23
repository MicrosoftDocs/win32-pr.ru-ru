---
description: Метод Get \_ девсинкоффсет извлекает стандартное отклонение времени в миллисекундах между временем выполнения каждого кадра и моментом его отрисовки для всех кадров с момента запуска потоковой передачи.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Метод CBaseVideoRenderer.get_DevSyncOffset (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657104"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="5abef-103">Кбасевидеорендерер. Get \_ девсинкоффсет, метод</span><span class="sxs-lookup"><span data-stu-id="5abef-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="5abef-104">`get_DevSyncOffset`Метод получает стандартное отклонение времени в миллисекундах между временем выполнения каждого кадра и моментом его отрисовки для всех кадров с момента запуска потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5abef-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="5abef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5abef-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="5abef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5abef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5abef-107">*пидев*</span><span class="sxs-lookup"><span data-stu-id="5abef-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="5abef-108">Указатель на стандартное отклонение времени, описанное ранее.</span><span class="sxs-lookup"><span data-stu-id="5abef-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5abef-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5abef-109">Return value</span></span>

<span data-ttu-id="5abef-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5abef-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5abef-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5abef-111">Remarks</span></span>

<span data-ttu-id="5abef-112">Эта функция члена реализует метод [**икуалпроп:: Get \_ девсинкоффсет**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="5abef-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5abef-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5abef-113">Requirements</span></span>



| <span data-ttu-id="5abef-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5abef-114">Requirement</span></span> | <span data-ttu-id="5abef-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5abef-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5abef-116">Header</span><span class="sxs-lookup"><span data-stu-id="5abef-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5abef-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5abef-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5abef-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5abef-118">Library</span></span><br/> | <dl> <span data-ttu-id="5abef-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5abef-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5abef-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5abef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abef-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="5abef-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




