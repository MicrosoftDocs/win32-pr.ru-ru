---
description: Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Ктрансформаутпутпин. Чеккмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658035"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="08015-103">Ктрансформаутпутпин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="08015-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="08015-104">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="08015-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="08015-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08015-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="08015-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08015-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08015-107">*мтин*</span><span class="sxs-lookup"><span data-stu-id="08015-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="08015-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="08015-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08015-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08015-109">Return value</span></span>

<span data-ttu-id="08015-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08015-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="08015-111">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="08015-111">Possible values include the following.</span></span>



| <span data-ttu-id="08015-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="08015-112">Return code</span></span>                                                                                  | <span data-ttu-id="08015-113">Описание</span><span class="sxs-lookup"><span data-stu-id="08015-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="08015-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="08015-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="08015-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="08015-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="08015-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="08015-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="08015-117">Входной ПИН-код фильтра не подключен.</span><span class="sxs-lookup"><span data-stu-id="08015-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08015-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08015-118">Remarks</span></span>

<span data-ttu-id="08015-119">Этот метод реализует чистый виртуальный метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="08015-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="08015-120">Метод завершается ошибкой, если входной ПИН-код фильтра не подключен.</span><span class="sxs-lookup"><span data-stu-id="08015-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="08015-121">В противном случае он вызывает метод [**ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) фильтра, который также является чистым виртуальным.</span><span class="sxs-lookup"><span data-stu-id="08015-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="08015-122">Производный класс фильтра должен реализовывать **чекктрансформ**, который определяет, совместим ли предложенный тип выходного носителя с входным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="08015-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="08015-123">Требования</span><span class="sxs-lookup"><span data-stu-id="08015-123">Requirements</span></span>



| <span data-ttu-id="08015-124">Требование</span><span class="sxs-lookup"><span data-stu-id="08015-124">Requirement</span></span> | <span data-ttu-id="08015-125">Значение</span><span class="sxs-lookup"><span data-stu-id="08015-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08015-126">Header</span><span class="sxs-lookup"><span data-stu-id="08015-126">Header</span></span><br/>  | <dl> <span data-ttu-id="08015-127"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08015-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="08015-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="08015-128">Library</span></span><br/> | <dl> <span data-ttu-id="08015-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="08015-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




