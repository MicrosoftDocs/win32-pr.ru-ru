---
description: Ктрансформинпутпин. Сетмедиатипе, метод Сетмедиатипе задает тип носителя для соединения.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Ктрансформинпутпин. Сетмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9af7310dbbf8830d7469c1a72ae43b946f1fbc69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095002"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="97fe3-103">Ктрансформинпутпин. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="97fe3-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="97fe3-104">`SetMediaType`Метод задает тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="97fe3-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fe3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97fe3-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="97fe3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97fe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97fe3-107">*машин*</span><span class="sxs-lookup"><span data-stu-id="97fe3-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="97fe3-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="97fe3-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97fe3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97fe3-109">Return value</span></span>

<span data-ttu-id="97fe3-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="97fe3-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="97fe3-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="97fe3-111">Remarks</span></span>

<span data-ttu-id="97fe3-112">Этот метод переопределяет метод [**кбасепин:: сетмедиатипе**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="97fe3-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="97fe3-113">Он вызывает метод [**ктрансформфилтер:: сетмедиатипе**](ctransformfilter-setmediatype.md) фильтра для информирования фильтра.</span><span class="sxs-lookup"><span data-stu-id="97fe3-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="97fe3-114">Перед вызовом этого метода ПИН-код должен проверить, является ли тип носителя приемлемым.</span><span class="sxs-lookup"><span data-stu-id="97fe3-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="97fe3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="97fe3-115">Requirements</span></span>



| <span data-ttu-id="97fe3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="97fe3-116">Requirement</span></span> | <span data-ttu-id="97fe3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="97fe3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97fe3-118">Header</span><span class="sxs-lookup"><span data-stu-id="97fe3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="97fe3-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97fe3-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97fe3-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97fe3-120">Library</span></span><br/> | <dl> <span data-ttu-id="97fe3-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="97fe3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




