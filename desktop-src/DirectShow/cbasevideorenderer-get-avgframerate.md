---
description: Метод Get \_ авгфрамерате вычисляет и получает среднюю частоту кадров.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Метод CBaseVideoRenderer.get_AvgFrameRate (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657788"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="7cd37-103">Кбасевидеорендерер. Get \_ авгфрамерате, метод</span><span class="sxs-lookup"><span data-stu-id="7cd37-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="7cd37-104">`get_AvgFrameRate`Метод вычисляет и получает среднюю частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="7cd37-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd37-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cd37-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="7cd37-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cd37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd37-107">*пиавгфрамерате*</span><span class="sxs-lookup"><span data-stu-id="7cd37-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd37-108">Указатель на число кадров в секунду с момента начала потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="7cd37-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd37-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cd37-109">Return value</span></span>

<span data-ttu-id="7cd37-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cd37-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd37-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cd37-111">Remarks</span></span>

<span data-ttu-id="7cd37-112">Эта функция члена реализует метод [**икуалпроп:: Get \_ авгфрамерате**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .</span><span class="sxs-lookup"><span data-stu-id="7cd37-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd37-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7cd37-113">Requirements</span></span>



| <span data-ttu-id="7cd37-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7cd37-114">Requirement</span></span> | <span data-ttu-id="7cd37-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd37-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd37-116">Header</span><span class="sxs-lookup"><span data-stu-id="7cd37-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7cd37-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cd37-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7cd37-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7cd37-118">Library</span></span><br/> | <dl> <span data-ttu-id="7cd37-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7cd37-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd37-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cd37-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd37-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="7cd37-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




