---
description: Метод Transform преобразует входной пример для создания примера вывода.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Метод Ктрансформфилтер. Transform (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675267"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="915bf-103">Ктрансформфилтер. Transform, метод</span><span class="sxs-lookup"><span data-stu-id="915bf-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="915bf-104">`Transform`Метод преобразует входной пример для создания примера вывода.</span><span class="sxs-lookup"><span data-stu-id="915bf-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="915bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="915bf-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="915bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="915bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="915bf-107">*ПИН*</span><span class="sxs-lookup"><span data-stu-id="915bf-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="915bf-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца входных данных.</span><span class="sxs-lookup"><span data-stu-id="915bf-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="915bf-109">*Тоска*</span><span class="sxs-lookup"><span data-stu-id="915bf-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="915bf-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца вывода.</span><span class="sxs-lookup"><span data-stu-id="915bf-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="915bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="915bf-111">Return value</span></span>

<span data-ttu-id="915bf-112">Базовый класс возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="915bf-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="915bf-113">Производный класс должен возвращать значение **HRESULT** , указывающее на успешное выполнение или ошибку.</span><span class="sxs-lookup"><span data-stu-id="915bf-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="915bf-114">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="915bf-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="915bf-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="915bf-115">Return code</span></span>                                                                             | <span data-ttu-id="915bf-116">Описание</span><span class="sxs-lookup"><span data-stu-id="915bf-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="915bf-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="915bf-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="915bf-118">Не Доставьте этот пример.</span><span class="sxs-lookup"><span data-stu-id="915bf-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="915bf-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="915bf-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="915bf-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="915bf-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="915bf-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="915bf-121">Remarks</span></span>

<span data-ttu-id="915bf-122">Переопределите этот метод для получения выходных данных.</span><span class="sxs-lookup"><span data-stu-id="915bf-122">Override this method to produce output data.</span></span> <span data-ttu-id="915bf-123">Считывает входные данные из образца, указанного параметром *ПИН-кода* , и записывает новые данные в образец, заданный параметром *тоска* .</span><span class="sxs-lookup"><span data-stu-id="915bf-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="915bf-124">Перед тем как фильтр вызовет этот метод, он копирует свойства из примера входных данных в образец Output.</span><span class="sxs-lookup"><span data-stu-id="915bf-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="915bf-125">`Transform`Метод должен устанавливать любые свойства, которые отличаются между двумя образцами, используя методы **имедиасампле** или интерфейс [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="915bf-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="915bf-126">Если фильтр не должен доставлять этот пример (например, для поддержки контроля качества), метод должен вернуть \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="915bf-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="915bf-127">Требования</span><span class="sxs-lookup"><span data-stu-id="915bf-127">Requirements</span></span>



| <span data-ttu-id="915bf-128">Требование</span><span class="sxs-lookup"><span data-stu-id="915bf-128">Requirement</span></span> | <span data-ttu-id="915bf-129">Значение</span><span class="sxs-lookup"><span data-stu-id="915bf-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="915bf-130">Header</span><span class="sxs-lookup"><span data-stu-id="915bf-130">Header</span></span><br/>  | <dl> <span data-ttu-id="915bf-131"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="915bf-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="915bf-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="915bf-132">Library</span></span><br/> | <dl> <span data-ttu-id="915bf-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="915bf-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="915bf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="915bf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915bf-135">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="915bf-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




