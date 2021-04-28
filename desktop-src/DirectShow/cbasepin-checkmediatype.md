---
description: Кбасепин. Чеккмедиатипе, метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Кбасепин. Чеккмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099401"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="55679-103">Кбасепин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="55679-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="55679-104">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="55679-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="55679-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55679-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="55679-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55679-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55679-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="55679-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="55679-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="55679-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55679-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55679-109">Return value</span></span>

<span data-ttu-id="55679-110">\_Если предложенный тип мультимедиа приемлем, возвращается значение S.</span><span class="sxs-lookup"><span data-stu-id="55679-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="55679-111">В противном случае возвращает \_ значение S false или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="55679-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55679-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="55679-112">Remarks</span></span>

<span data-ttu-id="55679-113">Производный класс должен переопределять этот чистый виртуальный метод.</span><span class="sxs-lookup"><span data-stu-id="55679-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="55679-114">Требования</span><span class="sxs-lookup"><span data-stu-id="55679-114">Requirements</span></span>



| <span data-ttu-id="55679-115">Требование</span><span class="sxs-lookup"><span data-stu-id="55679-115">Requirement</span></span> | <span data-ttu-id="55679-116">Значение</span><span class="sxs-lookup"><span data-stu-id="55679-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55679-117">Header</span><span class="sxs-lookup"><span data-stu-id="55679-117">Header</span></span><br/>  | <dl> <span data-ttu-id="55679-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55679-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55679-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55679-119">Library</span></span><br/> | <dl> <span data-ttu-id="55679-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="55679-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55679-121">См. также</span><span class="sxs-lookup"><span data-stu-id="55679-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55679-122">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="55679-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




