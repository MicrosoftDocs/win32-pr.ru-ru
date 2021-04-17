---
description: Метод Copy копирует пример носителя.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Метод Ктрансинплацефилтер. Copy (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679920"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="4caff-103">Ктрансинплацефилтер. Copy, метод</span><span class="sxs-lookup"><span data-stu-id="4caff-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="4caff-104">`Copy`Метод копирует пример носителя.</span><span class="sxs-lookup"><span data-stu-id="4caff-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="4caff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4caff-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="4caff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4caff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4caff-107">*псаурце*</span><span class="sxs-lookup"><span data-stu-id="4caff-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="4caff-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="4caff-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4caff-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4caff-109">Return value</span></span>

<span data-ttu-id="4caff-110">Возвращает указатель на интерфейс **имедиасампле** в новом образце.</span><span class="sxs-lookup"><span data-stu-id="4caff-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="4caff-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4caff-111">Remarks</span></span>

<span data-ttu-id="4caff-112">Этот метод извлекает пустой буфер из подчиненного распределителя.</span><span class="sxs-lookup"><span data-stu-id="4caff-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="4caff-113">Он копирует все примеры свойств из *псаурце* в новый образец вместе с реальными данными в примере.</span><span class="sxs-lookup"><span data-stu-id="4caff-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="4caff-114">Если фильтр использует два распределителя, он вызывает этот метод для копирования данных между буферами.</span><span class="sxs-lookup"><span data-stu-id="4caff-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="4caff-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4caff-115">Requirements</span></span>



| <span data-ttu-id="4caff-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4caff-116">Requirement</span></span> | <span data-ttu-id="4caff-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4caff-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caff-118">Header</span><span class="sxs-lookup"><span data-stu-id="4caff-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4caff-119"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4caff-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4caff-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4caff-120">Library</span></span><br/> | <dl> <span data-ttu-id="4caff-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4caff-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4caff-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4caff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4caff-123">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="4caff-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




