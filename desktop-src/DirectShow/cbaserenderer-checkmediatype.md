---
description: Метод Чеккмедиатипе определяет, принимает ли фильтр конкретный тип носителя.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Кбасерендерер. Чеккмедиатипе, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668748"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="31684-103">Кбасерендерер. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="31684-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="31684-104">`CheckMediaType`Метод определяет, принимает ли фильтр конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="31684-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="31684-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31684-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="31684-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31684-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="31684-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="31684-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31684-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31684-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31684-109">Return value</span></span>

<span data-ttu-id="31684-110">\_Если предложенный тип мультимедиа приемлем, возвращается значение S.</span><span class="sxs-lookup"><span data-stu-id="31684-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="31684-111">В противном случае возвращает \_ значение S false или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="31684-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31684-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31684-112">Remarks</span></span>

<span data-ttu-id="31684-113">Входной ПИН-код вызывает этот метод из собственного метода [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="31684-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="31684-114">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="31684-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31684-115">Требования</span><span class="sxs-lookup"><span data-stu-id="31684-115">Requirements</span></span>



| <span data-ttu-id="31684-116">Требование</span><span class="sxs-lookup"><span data-stu-id="31684-116">Requirement</span></span> | <span data-ttu-id="31684-117">Значение</span><span class="sxs-lookup"><span data-stu-id="31684-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31684-118">Header</span><span class="sxs-lookup"><span data-stu-id="31684-118">Header</span></span><br/>  | <dl> <span data-ttu-id="31684-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31684-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31684-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31684-120">Library</span></span><br/> | <dl> <span data-ttu-id="31684-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="31684-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31684-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31684-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31684-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="31684-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




