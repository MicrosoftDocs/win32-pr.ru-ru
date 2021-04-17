---
description: Метод Сетмедиатипе задает тип носителя для соединения.
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
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657665"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="7d78c-103">Кбасепин. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="7d78c-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="7d78c-104">`SetMediaType`Метод задает тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="7d78c-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d78c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d78c-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7d78c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d78c-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="7d78c-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7d78c-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7d78c-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d78c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d78c-109">Return value</span></span>

<span data-ttu-id="7d78c-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7d78c-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d78c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d78c-111">Remarks</span></span>

<span data-ttu-id="7d78c-112">Этот метод устанавливает формат для соединения с закреплением.</span><span class="sxs-lookup"><span data-stu-id="7d78c-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="7d78c-113">Перед вызовом этого метода ПИН-код вызывает метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) , чтобы определить, является ли тип мультимедиа допустимым.</span><span class="sxs-lookup"><span data-stu-id="7d78c-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="7d78c-114">Поэтому предполагается, что параметр *ПЛТ* является допустимым типом носителя.</span><span class="sxs-lookup"><span data-stu-id="7d78c-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="7d78c-115">В базовом классе этот метод задает переменную члена [**кбасепин:: m \_ MT**](cbasepin-m-mt.md) и возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7d78c-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="7d78c-116">Производный класс может переопределить этот метод, если он требует уведомления, если задан тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7d78c-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d78c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7d78c-117">Requirements</span></span>



| <span data-ttu-id="7d78c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7d78c-118">Requirement</span></span> | <span data-ttu-id="7d78c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7d78c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d78c-120">Header</span><span class="sxs-lookup"><span data-stu-id="7d78c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7d78c-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d78c-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7d78c-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7d78c-122">Library</span></span><br/> | <dl> <span data-ttu-id="7d78c-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7d78c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d78c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d78c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d78c-125">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="7d78c-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




