---
description: 'Метод Сетмедиатипе задает тип носителя для соединения. Этот метод переопределяет метод Кбасепин:: Сетмедиатипе.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Крендереринпутпин. Сетмедиатипе, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669368"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="07118-104">Крендереринпутпин. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="07118-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="07118-105">`SetMediaType`Метод задает тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="07118-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="07118-106">Этот метод переопределяет метод [**кбасепин:: сетмедиатипе**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="07118-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07118-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07118-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="07118-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="07118-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07118-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="07118-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="07118-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="07118-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07118-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07118-111">Return value</span></span>

<span data-ttu-id="07118-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07118-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="07118-113">Требования</span><span class="sxs-lookup"><span data-stu-id="07118-113">Requirements</span></span>



| <span data-ttu-id="07118-114">Требование</span><span class="sxs-lookup"><span data-stu-id="07118-114">Requirement</span></span> | <span data-ttu-id="07118-115">Значение</span><span class="sxs-lookup"><span data-stu-id="07118-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07118-116">Header</span><span class="sxs-lookup"><span data-stu-id="07118-116">Header</span></span><br/>  | <dl> <span data-ttu-id="07118-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07118-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07118-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07118-118">Library</span></span><br/> | <dl> <span data-ttu-id="07118-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="07118-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07118-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07118-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07118-121">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="07118-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




