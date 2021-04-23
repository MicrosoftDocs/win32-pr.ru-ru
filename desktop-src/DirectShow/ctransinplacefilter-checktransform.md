---
description: 'Метод Чекктрансформ проверяет, совместим ли входной тип носителя с выходным типом носителя. Этот метод переопределяет метод Ктрансформфилтер:: Чекктрансформ.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Ктрансинплацефилтер. Чекктрансформ, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679921"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="d4b53-104">Ктрансинплацефилтер. Чекктрансформ, метод</span><span class="sxs-lookup"><span data-stu-id="d4b53-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="d4b53-105">`CheckTransform`Метод проверяет, совместим ли входной тип носителя с выходным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="d4b53-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="d4b53-106">Этот метод переопределяет метод [**ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="d4b53-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b53-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4b53-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="d4b53-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4b53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b53-109">*мтин*</span><span class="sxs-lookup"><span data-stu-id="d4b53-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b53-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="d4b53-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="d4b53-111">*мтаут*</span><span class="sxs-lookup"><span data-stu-id="d4b53-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b53-112">Указатель на объект **кмедиатипе** , указывающий тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d4b53-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b53-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4b53-113">Return value</span></span>

<span data-ttu-id="d4b53-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d4b53-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b53-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4b53-115">Remarks</span></span>

<span data-ttu-id="d4b53-116">Фильтр **ктрансинплаце** никогда не вызывает `CheckTransform` .</span><span class="sxs-lookup"><span data-stu-id="d4b53-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="d4b53-117">Вместо этого все соединения с ПИН-кодом используют [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) для проверки типа мультимедиа, предположение, что типы входных и выходных данных всегда совпадают.</span><span class="sxs-lookup"><span data-stu-id="d4b53-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b53-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d4b53-118">Requirements</span></span>



| <span data-ttu-id="d4b53-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d4b53-119">Requirement</span></span> | <span data-ttu-id="d4b53-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d4b53-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b53-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4b53-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d4b53-122"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b53-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4b53-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4b53-123">Library</span></span><br/> | <dl> <span data-ttu-id="d4b53-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b53-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b53-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4b53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b53-126">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="d4b53-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




