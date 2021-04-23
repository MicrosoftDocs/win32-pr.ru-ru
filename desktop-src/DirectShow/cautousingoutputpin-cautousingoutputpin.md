---
description: Метод конструктора. Конструктор получает доступ к указанному ПИН-коду.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Конструктор Каутаусингаутпутпин. Каутаусингаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657855"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="9f86d-104">Каутаусингаутпутпин. Каутаусингаутпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="9f86d-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="9f86d-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="9f86d-105">Constructor method.</span></span> <span data-ttu-id="9f86d-106">Конструктор получает доступ к указанному ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="9f86d-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f86d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f86d-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="9f86d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f86d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f86d-109">*паутпутпин*</span><span class="sxs-lookup"><span data-stu-id="9f86d-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9f86d-110">Указатель на объект [**кдинамикаутпутпин**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="9f86d-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9f86d-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="9f86d-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9f86d-112">Указатель на переменную, содержащую значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f86d-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="9f86d-113">Значение должно быть равно "S" \_ .</span><span class="sxs-lookup"><span data-stu-id="9f86d-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f86d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f86d-114">Remarks</span></span>

<span data-ttu-id="9f86d-115">При возврате из метода значение *\* фр* указывает на успешное или неуспешное завершение метода.</span><span class="sxs-lookup"><span data-stu-id="9f86d-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f86d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9f86d-116">Requirements</span></span>



| <span data-ttu-id="9f86d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9f86d-117">Requirement</span></span> | <span data-ttu-id="9f86d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9f86d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f86d-119">Header</span><span class="sxs-lookup"><span data-stu-id="9f86d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9f86d-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f86d-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f86d-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f86d-121">Library</span></span><br/> | <dl> <span data-ttu-id="9f86d-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9f86d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f86d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f86d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f86d-124">**Класс Каутаусингаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="9f86d-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




