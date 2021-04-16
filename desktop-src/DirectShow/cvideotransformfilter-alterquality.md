---
description: 'Метод Алтеркуалити уведомляет фильтр о том, что запрошено изменение качества. Этот метод переопределяет метод Ктрансформфилтер:: Алтеркуалити.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Квидеотрансформфилтер. Алтеркуалити, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656847"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="68fcb-104">Квидеотрансформфилтер. Алтеркуалити, метод</span><span class="sxs-lookup"><span data-stu-id="68fcb-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="68fcb-105">`AlterQuality`Метод уведомляет фильтр о запросе изменения качества.</span><span class="sxs-lookup"><span data-stu-id="68fcb-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="68fcb-106">Этот метод переопределяет метод [**ктрансформфилтер:: алтеркуалити**](ctransformfilter-alterquality.md) .</span><span class="sxs-lookup"><span data-stu-id="68fcb-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fcb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68fcb-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="68fcb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68fcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68fcb-109">*формате*</span><span class="sxs-lookup"><span data-stu-id="68fcb-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="68fcb-110">Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="68fcb-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68fcb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68fcb-111">Return value</span></span>

<span data-ttu-id="68fcb-112">Возвращает значение E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="68fcb-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="68fcb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68fcb-113">Remarks</span></span>

<span data-ttu-id="68fcb-114">Этот метод вызывается, когда выходной ПИН-код получает качественное сообщение (с помощью метода [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).</span><span class="sxs-lookup"><span data-stu-id="68fcb-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="68fcb-115">Значение опоздания из *q* хранится в переменной-члене **m \_ итрлате** .</span><span class="sxs-lookup"><span data-stu-id="68fcb-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="68fcb-116">Возвращаемое значение E \_ Fail означает, что модуль подготовки отчетов должен перехватить кадры, хотя класс **квидеотрансформфилтер** также будет удалять фреймы под правильными условиями.</span><span class="sxs-lookup"><span data-stu-id="68fcb-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="68fcb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="68fcb-117">Requirements</span></span>



| <span data-ttu-id="68fcb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="68fcb-118">Requirement</span></span> | <span data-ttu-id="68fcb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="68fcb-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68fcb-120">Header</span><span class="sxs-lookup"><span data-stu-id="68fcb-120">Header</span></span><br/>  | <dl> <span data-ttu-id="68fcb-121"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68fcb-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="68fcb-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68fcb-122">Library</span></span><br/> | <dl> <span data-ttu-id="68fcb-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="68fcb-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68fcb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68fcb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fcb-125">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="68fcb-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="68fcb-126">**Квидеотрансформфилтер:: Шаулдскипфраме**</span><span class="sxs-lookup"><span data-stu-id="68fcb-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




