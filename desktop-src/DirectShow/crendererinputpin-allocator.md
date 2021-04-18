---
description: Метод распределителя извлекает указатель на распределитель памяти.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Метод Крендереринпутпин. распределитель (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668653"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="0a468-103">Крендереринпутпин. распределитель, метод</span><span class="sxs-lookup"><span data-stu-id="0a468-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="0a468-104">`Allocator`Метод получает указатель на распределитель памяти.</span><span class="sxs-lookup"><span data-stu-id="0a468-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a468-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a468-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="0a468-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a468-106">Parameters</span></span>

<span data-ttu-id="0a468-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0a468-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a468-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a468-108">Return value</span></span>

<span data-ttu-id="0a468-109">Возвращает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a468-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a468-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a468-110">Remarks</span></span>

<span data-ttu-id="0a468-111">Этот метод возвращает переменную члена [**кбасеинпутпин:: m \_ паллокатор**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="0a468-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="0a468-112">Метод не увеличивает значение счетчика ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="0a468-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="0a468-113">Этот метод является исключительно методом доступа.</span><span class="sxs-lookup"><span data-stu-id="0a468-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a468-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0a468-114">Requirements</span></span>



| <span data-ttu-id="0a468-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0a468-115">Requirement</span></span> | <span data-ttu-id="0a468-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0a468-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a468-117">Header</span><span class="sxs-lookup"><span data-stu-id="0a468-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0a468-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a468-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a468-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a468-119">Library</span></span><br/> | <dl> <span data-ttu-id="0a468-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0a468-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a468-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a468-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a468-122">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="0a468-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




