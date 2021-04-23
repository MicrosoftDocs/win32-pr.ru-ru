---
description: Метод Сетмедиатипе вызывается, когда задан тип носителя ПИН-кода.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Кбасерендерер. Сетмедиатипе, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669344"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="64ca0-103">Кбасерендерер. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="64ca0-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="64ca0-104">`SetMediaType`Метод вызывается, когда задан тип носителя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="64ca0-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ca0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64ca0-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="64ca0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64ca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64ca0-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="64ca0-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="64ca0-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="64ca0-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64ca0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64ca0-109">Return value</span></span>

<span data-ttu-id="64ca0-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="64ca0-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ca0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64ca0-111">Remarks</span></span>

<span data-ttu-id="64ca0-112">Входной ПИН-код вызывает этот метод из собственного метода [**крендереринпутпин:: сетмедиатипе**](crendererinputpin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="64ca0-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="64ca0-113">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="64ca0-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="64ca0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="64ca0-114">Requirements</span></span>



| <span data-ttu-id="64ca0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="64ca0-115">Requirement</span></span> | <span data-ttu-id="64ca0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="64ca0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ca0-117">Header</span><span class="sxs-lookup"><span data-stu-id="64ca0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="64ca0-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64ca0-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="64ca0-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64ca0-119">Library</span></span><br/> | <dl> <span data-ttu-id="64ca0-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="64ca0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ca0-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64ca0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ca0-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="64ca0-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




