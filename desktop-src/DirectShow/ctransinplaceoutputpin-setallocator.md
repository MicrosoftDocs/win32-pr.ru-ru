---
description: Метод Сеталлокатор задает распределитель для соединения.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Ктрансинплацеаутпутпин. Сеталлокатор, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657078"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="af5ca-103">Ктрансинплацеаутпутпин. Сеталлокатор, метод</span><span class="sxs-lookup"><span data-stu-id="af5ca-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="af5ca-104">`SetAllocator`Метод задает распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="af5ca-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="af5ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af5ca-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="af5ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af5ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af5ca-107">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="af5ca-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="af5ca-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="af5ca-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af5ca-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af5ca-109">Return value</span></span>

<span data-ttu-id="af5ca-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="af5ca-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af5ca-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af5ca-111">Remarks</span></span>

<span data-ttu-id="af5ca-112">Закрепление вывода для этого фильтра никогда не предоставляет распределитель.</span><span class="sxs-lookup"><span data-stu-id="af5ca-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="af5ca-113">Этот метод задает распределитель для выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="af5ca-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="af5ca-114">Он задает значение переменной члена [**кбасеаутпутпин:: m \_ паллокатор**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="af5ca-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5ca-115">Требования</span><span class="sxs-lookup"><span data-stu-id="af5ca-115">Requirements</span></span>



| <span data-ttu-id="af5ca-116">Требование</span><span class="sxs-lookup"><span data-stu-id="af5ca-116">Requirement</span></span> | <span data-ttu-id="af5ca-117">Значение</span><span class="sxs-lookup"><span data-stu-id="af5ca-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af5ca-118">Header</span><span class="sxs-lookup"><span data-stu-id="af5ca-118">Header</span></span><br/>  | <dl> <span data-ttu-id="af5ca-119"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af5ca-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af5ca-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af5ca-120">Library</span></span><br/> | <dl> <span data-ttu-id="af5ca-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="af5ca-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5ca-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af5ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5ca-123">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="af5ca-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




