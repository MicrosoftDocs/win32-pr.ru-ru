---
description: Метод Transform преобразует образец на месте.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Метод Ктрансинплацефилтер. Transform (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680088"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="c1935-103">Ктрансинплацефилтер. Transform, метод</span><span class="sxs-lookup"><span data-stu-id="c1935-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="c1935-104">`Transform`Метод преобразует образец на месте.</span><span class="sxs-lookup"><span data-stu-id="c1935-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1935-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1935-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c1935-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1935-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="c1935-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c1935-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="c1935-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1935-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1935-109">Return value</span></span>

<span data-ttu-id="c1935-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1935-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c1935-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c1935-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c1935-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c1935-112">Return code</span></span>                                                                             | <span data-ttu-id="c1935-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c1935-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="c1935-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c1935-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c1935-115">Не Доставьте этот пример.</span><span class="sxs-lookup"><span data-stu-id="c1935-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="c1935-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c1935-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c1935-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c1935-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c1935-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1935-118">Remarks</span></span>

<span data-ttu-id="c1935-119">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="c1935-119">The derived class must implement this method.</span></span> <span data-ttu-id="c1935-120">Преобразуйте образец данных на месте.</span><span class="sxs-lookup"><span data-stu-id="c1935-120">Transform the sample data in place.</span></span> <span data-ttu-id="c1935-121">Если фильтр использует два распределителя, он копирует данные из входного примера в новый пример и передает копию в этот метод.</span><span class="sxs-lookup"><span data-stu-id="c1935-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="c1935-122">Если фильтр не должен доставлять этот пример (например, для поддержки контроля качества), метод должен вернуть \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="c1935-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1935-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c1935-123">Requirements</span></span>



| <span data-ttu-id="c1935-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c1935-124">Requirement</span></span> | <span data-ttu-id="c1935-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c1935-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1935-126">Header</span><span class="sxs-lookup"><span data-stu-id="c1935-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c1935-127"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1935-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1935-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1935-128">Library</span></span><br/> | <dl> <span data-ttu-id="c1935-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c1935-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1935-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1935-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1935-131">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="c1935-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




