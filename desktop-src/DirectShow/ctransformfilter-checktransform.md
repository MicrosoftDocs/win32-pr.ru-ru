---
description: Метод Чекктрансформ проверяет, совместим ли входной тип носителя с выходным типом носителя.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Ктрансформфилтер. Чекктрансформ, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657453"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="d9030-103">Ктрансформфилтер. Чекктрансформ, метод</span><span class="sxs-lookup"><span data-stu-id="d9030-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="d9030-104">`CheckTransform`Метод проверяет, совместим ли входной тип носителя с выходным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="d9030-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9030-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9030-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d9030-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9030-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9030-107">*мтин*</span><span class="sxs-lookup"><span data-stu-id="d9030-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="d9030-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="d9030-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="d9030-109">*мтаут*</span><span class="sxs-lookup"><span data-stu-id="d9030-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="d9030-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d9030-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9030-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9030-111">Return value</span></span>

<span data-ttu-id="d9030-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9030-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d9030-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d9030-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d9030-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d9030-114">Return code</span></span>                                                                                                | <span data-ttu-id="d9030-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d9030-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d9030-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d9030-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="d9030-117">Типы мультимедиа совместимы.</span><span class="sxs-lookup"><span data-stu-id="d9030-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="d9030-118"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="d9030-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="d9030-119">Типы мультимедиа несовместимы.</span><span class="sxs-lookup"><span data-stu-id="d9030-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9030-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9030-120">Remarks</span></span>

<span data-ttu-id="d9030-121">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="d9030-121">The derived class must implement this method.</span></span> <span data-ttu-id="d9030-122">Возврат \_ ОК, если фильтр может принимать оба указанных типа мультимедиа или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d9030-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9030-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d9030-123">Requirements</span></span>



| <span data-ttu-id="d9030-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d9030-124">Requirement</span></span> | <span data-ttu-id="d9030-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d9030-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9030-126">Header</span><span class="sxs-lookup"><span data-stu-id="d9030-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d9030-127"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9030-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9030-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9030-128">Library</span></span><br/> | <dl> <span data-ttu-id="d9030-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d9030-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




