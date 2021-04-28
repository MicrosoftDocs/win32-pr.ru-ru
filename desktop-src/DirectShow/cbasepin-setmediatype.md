---
description: Кбасепин. Сетмедиатипе, метод Сетмедиатипе задает тип носителя для соединения.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Кбасепин. Сетмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095991"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="6b569-103">Кбасепин. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="6b569-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="6b569-104">`SetMediaType`Метод задает тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="6b569-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b569-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b569-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6b569-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b569-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b569-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="6b569-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6b569-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6b569-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b569-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b569-109">Return value</span></span>

<span data-ttu-id="6b569-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6b569-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b569-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="6b569-111">Remarks</span></span>

<span data-ttu-id="6b569-112">Этот метод устанавливает формат для соединения с закреплением.</span><span class="sxs-lookup"><span data-stu-id="6b569-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="6b569-113">Перед вызовом этого метода ПИН-код вызывает метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) , чтобы определить, является ли тип мультимедиа допустимым.</span><span class="sxs-lookup"><span data-stu-id="6b569-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="6b569-114">Поэтому предполагается, что параметр *ПЛТ* является допустимым типом носителя.</span><span class="sxs-lookup"><span data-stu-id="6b569-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="6b569-115">В базовом классе этот метод задает переменную члена [**кбасепин:: m \_ MT**](cbasepin-m-mt.md) и возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6b569-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="6b569-116">Производный класс может переопределить этот метод, если он требует уведомления, если задан тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6b569-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b569-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6b569-117">Requirements</span></span>



| <span data-ttu-id="6b569-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6b569-118">Requirement</span></span> | <span data-ttu-id="6b569-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6b569-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b569-120">Header</span><span class="sxs-lookup"><span data-stu-id="6b569-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6b569-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b569-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6b569-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b569-122">Library</span></span><br/> | <dl> <span data-ttu-id="6b569-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6b569-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b569-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6b569-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b569-125">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="6b569-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




