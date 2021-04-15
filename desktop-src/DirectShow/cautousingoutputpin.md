---
description: Класс Каутаусингаутпутпин получает и освобождает доступ к объекту Кдинамикаутпутпин.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Класс Каутаусингаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669149"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="3d9a0-103">Класс Каутаусингаутпутпин</span><span class="sxs-lookup"><span data-stu-id="3d9a0-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="3d9a0-104">Класс **каутаусингаутпутпин** получает и освобождает доступ к объекту [**кдинамикаутпутпин**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="3d9a0-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="3d9a0-105">**Каутаусингаутпутпин** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3d9a0-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="3d9a0-106">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="3d9a0-106">Public Methods</span></span>                                                           | <span data-ttu-id="3d9a0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3d9a0-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="3d9a0-108">**каутаусингаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="3d9a0-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="3d9a0-109">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="3d9a0-109">Constructor method.</span></span> <span data-ttu-id="3d9a0-110">Получает доступ к указанному ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="3d9a0-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="3d9a0-111">**~ Каутаусингаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="3d9a0-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="3d9a0-112">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="3d9a0-112">Destructor method.</span></span> <span data-ttu-id="3d9a0-113">Получает доступ к указанному ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="3d9a0-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="3d9a0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d9a0-114">Remarks</span></span>

<span data-ttu-id="3d9a0-115">При вызове определенных методов для [**кдинамикаутпутпин**](cdynamicoutputpin.md)вызывающий должен получить доступ к ПИН-коду, а затем освободить этот доступ.</span><span class="sxs-lookup"><span data-stu-id="3d9a0-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="3d9a0-116">Для получения доступа вызывающий объект использует метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="3d9a0-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="3d9a0-117">Чтобы освободить доступ, он вызывает метод [**кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="3d9a0-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="3d9a0-118">Класс **каутаусингаутпутпин** является вспомогательным классом, который обрабатывает эти задачи в конструкторе и методах деструктора.</span><span class="sxs-lookup"><span data-stu-id="3d9a0-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="3d9a0-119">В следующем примере кода показано, как использовать этот класс:</span><span class="sxs-lookup"><span data-stu-id="3d9a0-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="3d9a0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3d9a0-120">Requirements</span></span>



| <span data-ttu-id="3d9a0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3d9a0-121">Requirement</span></span> | <span data-ttu-id="3d9a0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3d9a0-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9a0-123">Header</span><span class="sxs-lookup"><span data-stu-id="3d9a0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3d9a0-124"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d9a0-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3d9a0-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3d9a0-125">Library</span></span><br/> | <dl> <span data-ttu-id="3d9a0-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3d9a0-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d9a0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d9a0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d9a0-128">Ссылка на базовый класс</span><span class="sxs-lookup"><span data-stu-id="3d9a0-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




