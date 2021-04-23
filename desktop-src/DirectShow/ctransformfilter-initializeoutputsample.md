---
description: Метод Инитиализеаутпутсампле извлекает новый образец вывода и инициализирует его.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Iniметод Тиализеаутпутсампле (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657756"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="81f28-103">CTransformFilter.Iniметод Тиализеаутпутсампле</span><span class="sxs-lookup"><span data-stu-id="81f28-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="81f28-104">`InitializeOutputSample`Метод получает новый выходной пример и инициализирует его.</span><span class="sxs-lookup"><span data-stu-id="81f28-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81f28-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="81f28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81f28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f28-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="81f28-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="81f28-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца входных данных.</span><span class="sxs-lookup"><span data-stu-id="81f28-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="81f28-109">*ппаутсампле*</span><span class="sxs-lookup"><span data-stu-id="81f28-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="81f28-110">Получает указатель на интерфейс **имедиасампле** образца выходных данных.</span><span class="sxs-lookup"><span data-stu-id="81f28-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81f28-111">Return value</span></span>

<span data-ttu-id="81f28-112">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81f28-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f28-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81f28-113">Remarks</span></span>

<span data-ttu-id="81f28-114">Этот метод вызывается методом [**ктрансформфилтер:: Receive**](ctransformfilter-receive.md) для подготовки выходного примера.</span><span class="sxs-lookup"><span data-stu-id="81f28-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="81f28-115">Как правило, нет необходимости вызывать этот метод в производном классе, если не переопределить метод **Receive** .</span><span class="sxs-lookup"><span data-stu-id="81f28-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="81f28-116">Этот метод получает новый пример из распределителя выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="81f28-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="81f28-117">Затем он копирует примеры свойств из примера входных данных в образец Output.</span><span class="sxs-lookup"><span data-stu-id="81f28-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="81f28-118">Примеры свойств определяются в структуре [**\_ \_ свойств SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="81f28-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="81f28-119">Требования</span><span class="sxs-lookup"><span data-stu-id="81f28-119">Requirements</span></span>



| <span data-ttu-id="81f28-120">Требование</span><span class="sxs-lookup"><span data-stu-id="81f28-120">Requirement</span></span> | <span data-ttu-id="81f28-121">Значение</span><span class="sxs-lookup"><span data-stu-id="81f28-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81f28-122">Header</span><span class="sxs-lookup"><span data-stu-id="81f28-122">Header</span></span><br/>  | <dl> <span data-ttu-id="81f28-123"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81f28-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81f28-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81f28-124">Library</span></span><br/> | <dl> <span data-ttu-id="81f28-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="81f28-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f28-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81f28-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f28-127">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="81f28-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




