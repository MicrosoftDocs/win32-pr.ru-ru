---
description: Метод получения \_ колебаний получает стандартное отклонение времени в миллисекундах между кадром и следующим для всех кадров с момента запуска потоковой передачи.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Метод CBaseVideoRenderer.get_Jitter (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675209"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="2a343-103">Кбасевидеорендерер. получение \_ метода противосинхронизации</span><span class="sxs-lookup"><span data-stu-id="2a343-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="2a343-104">`get_Jitter`Метод получает стандартное отклонение времени в миллисекундах между каждым кадром и следующим для всех кадров с момента запуска потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="2a343-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a343-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a343-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="2a343-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a343-107">*пижиттер*</span><span class="sxs-lookup"><span data-stu-id="2a343-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="2a343-108">Указатель на стандартное отклонение времени между кадрами в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="2a343-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a343-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a343-109">Return value</span></span>

<span data-ttu-id="2a343-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a343-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a343-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a343-111">Remarks</span></span>

<span data-ttu-id="2a343-112">Эта функция члена реализует метод [**\_ колебаний икуалпроп:: Get**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .</span><span class="sxs-lookup"><span data-stu-id="2a343-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a343-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2a343-113">Requirements</span></span>



| <span data-ttu-id="2a343-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2a343-114">Requirement</span></span> | <span data-ttu-id="2a343-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2a343-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a343-116">Header</span><span class="sxs-lookup"><span data-stu-id="2a343-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2a343-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a343-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2a343-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a343-118">Library</span></span><br/> | <dl> <span data-ttu-id="2a343-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2a343-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a343-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a343-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a343-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="2a343-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




