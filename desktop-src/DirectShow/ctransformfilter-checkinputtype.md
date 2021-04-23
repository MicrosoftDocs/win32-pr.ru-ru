---
description: Метод Чеккинпуттипе проверяет, допустим ли указанный тип носителя для входных данных.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Ктрансформфилтер. Чеккинпуттипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657023"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="1ef2f-103">Ктрансформфилтер. Чеккинпуттипе, метод</span><span class="sxs-lookup"><span data-stu-id="1ef2f-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="1ef2f-104">`CheckInputType`Метод проверяет, допустим ли указанный тип носителя для входных данных.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ef2f-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="1ef2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ef2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef2f-107">*мтин*</span><span class="sxs-lookup"><span data-stu-id="1ef2f-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="1ef2f-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef2f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ef2f-109">Return value</span></span>

<span data-ttu-id="1ef2f-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ef2f-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ef2f-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1ef2f-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1ef2f-112">Return code</span></span>                                                                                                | <span data-ttu-id="1ef2f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1ef2f-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="1ef2f-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ef2f-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1ef2f-115">Допустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="1ef2f-116"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="1ef2f-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="1ef2f-117">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ef2f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ef2f-118">Remarks</span></span>

<span data-ttu-id="1ef2f-119">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-119">The derived class must implement this method.</span></span> <span data-ttu-id="1ef2f-120">Возвращает значение \_ ОК, если предложенный входной формат допустим, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1ef2f-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="1ef2f-121">Этому методу не нужно проверять, совместим ли входной формат с выходным форматом (если он есть).</span><span class="sxs-lookup"><span data-stu-id="1ef2f-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="1ef2f-122">Входной ПИН-код проверяет это, вызывая метод [**чекктрансформ**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef2f-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef2f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1ef2f-123">Requirements</span></span>



| <span data-ttu-id="1ef2f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1ef2f-124">Requirement</span></span> | <span data-ttu-id="1ef2f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1ef2f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef2f-126">Header</span><span class="sxs-lookup"><span data-stu-id="1ef2f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1ef2f-127"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ef2f-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1ef2f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ef2f-128">Library</span></span><br/> | <dl> <span data-ttu-id="1ef2f-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1ef2f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef2f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ef2f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef2f-131">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="1ef2f-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




