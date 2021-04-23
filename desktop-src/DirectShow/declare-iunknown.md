---
description: Макрос DECLARE \_ IUnknown объявляет три метода базового интерфейса для нового интерфейса.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657711"
---
# <a name="declare_iunknown"></a><span data-ttu-id="200d6-103">ОБЪЯВЛЕНИЕ \_ IUnknown</span><span class="sxs-lookup"><span data-stu-id="200d6-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="200d6-104">Макрос **Declare \_ IUnknown** объявляет три метода базового интерфейса для нового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="200d6-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="200d6-105">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="200d6-105">**Syntax**</span></span>

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a><span data-ttu-id="200d6-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="200d6-106">Remarks</span></span>

<span data-ttu-id="200d6-107">При создании нового интерфейса он должен быть производным от **IUnknown**, который имеет три метода: **QueryInterface**, **AddRef** и **Release**.</span><span class="sxs-lookup"><span data-stu-id="200d6-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="200d6-108">Этот макрос упрощает процесс объявления, объявляя каждый из этих методов для нового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="200d6-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="200d6-109">Этот макрос работает только с классами, которые прямо или косвенно являются производными от класса [**кункновн**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="200d6-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="200d6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="200d6-110">Requirements</span></span>



| <span data-ttu-id="200d6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="200d6-111">Requirement</span></span> | <span data-ttu-id="200d6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="200d6-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200d6-113">Header</span><span class="sxs-lookup"><span data-stu-id="200d6-113">Header</span></span><br/>  | <dl> <span data-ttu-id="200d6-114"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="200d6-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="200d6-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="200d6-115">Library</span></span><br/> | <dl> <span data-ttu-id="200d6-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="200d6-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200d6-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="200d6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200d6-118">**Вспомогательные функции COM**</span><span class="sxs-lookup"><span data-stu-id="200d6-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="200d6-119">**Кункновн:: owner**</span><span class="sxs-lookup"><span data-stu-id="200d6-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="200d6-120">Реализация IUnknown</span><span class="sxs-lookup"><span data-stu-id="200d6-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




