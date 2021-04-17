---
description: Метод CreateInstance создает экземпляр объекта. Этот метод поддерживает создание объекта с помощью фабрики классов. Дополнительные сведения см. в разделе Кфакторитемплате.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Метод Ксикингпасссру. CreateInstance (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657272"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="202d4-105">Ксикингпасссру. CreateInstance, метод</span><span class="sxs-lookup"><span data-stu-id="202d4-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="202d4-106">`CreateInstance`Метод создает экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="202d4-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="202d4-107">Этот метод поддерживает создание объекта с помощью фабрики классов.</span><span class="sxs-lookup"><span data-stu-id="202d4-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="202d4-108">Дополнительные сведения см. в разделе [**кфакторитемплате**](cfactorytemplate.md).</span><span class="sxs-lookup"><span data-stu-id="202d4-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="202d4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="202d4-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="202d4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="202d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202d4-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="202d4-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="202d4-112">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="202d4-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="202d4-113">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="202d4-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="202d4-114">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="202d4-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="202d4-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="202d4-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="202d4-116">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="202d4-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="202d4-117">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="202d4-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202d4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="202d4-118">Return value</span></span>

<span data-ttu-id="202d4-119">Возвращает указатель на новый объект **ксикингпасссру** .</span><span class="sxs-lookup"><span data-stu-id="202d4-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="202d4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="202d4-120">Requirements</span></span>



| <span data-ttu-id="202d4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="202d4-121">Requirement</span></span> | <span data-ttu-id="202d4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="202d4-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202d4-123">Header</span><span class="sxs-lookup"><span data-stu-id="202d4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="202d4-124"><dt>Сикпт. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="202d4-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="202d4-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="202d4-125">Library</span></span><br/> | <dl> <span data-ttu-id="202d4-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="202d4-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202d4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="202d4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202d4-128">**Класс Ксикингпасссру**</span><span class="sxs-lookup"><span data-stu-id="202d4-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




