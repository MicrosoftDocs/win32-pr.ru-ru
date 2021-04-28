---
description: Ктрансинплацеинпутпин. метод распределителя — метод метода распределителя извлекает распределитель памяти, предложенный этим ПИН-кодом. Этот метод реализует метод Имеминпутпин::/распределителя.
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Метод Ктрансинплацеинпутпин. методом перераспределения (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084662"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="b38d9-104">Ктрансинплацеинпутпин. метод распределения</span><span class="sxs-lookup"><span data-stu-id="b38d9-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="b38d9-105">`GetAllocator`Метод извлекает распределитель памяти, предложенный этим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="b38d9-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="b38d9-106">Этот метод реализует метод [**имеминпутпин::/распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="b38d9-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b38d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b38d9-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="b38d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b38d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b38d9-109">*ппаллокатор*</span><span class="sxs-lookup"><span data-stu-id="b38d9-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="b38d9-110">Получает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="b38d9-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b38d9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b38d9-111">Return value</span></span>

<span data-ttu-id="b38d9-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b38d9-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b38d9-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b38d9-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b38d9-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b38d9-114">Return code</span></span>                                                                                          | <span data-ttu-id="b38d9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b38d9-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b38d9-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b38d9-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="b38d9-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b38d9-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="b38d9-118"><dt>**VFW \_ E \_ без \_ распределителя**</dt></span><span class="sxs-lookup"><span data-stu-id="b38d9-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="b38d9-119">Распределитель недоступен.</span><span class="sxs-lookup"><span data-stu-id="b38d9-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b38d9-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="b38d9-120">Remarks</span></span>

<span data-ttu-id="b38d9-121">Если закрепление вывода фильтра подключено, этот метод запрашивает распределитель из входного ПИН-кода подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="b38d9-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="b38d9-122">Если закрепление вывода фильтра не подключено, этот метод создает временный распределитель.</span><span class="sxs-lookup"><span data-stu-id="b38d9-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="b38d9-123">Позже, когда закрепление вывода будет подключено, фильтр повторно подключится к входному ПИН-коду и заново согласовывать распределитель.</span><span class="sxs-lookup"><span data-stu-id="b38d9-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="b38d9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b38d9-124">Requirements</span></span>



| <span data-ttu-id="b38d9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b38d9-125">Requirement</span></span> | <span data-ttu-id="b38d9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b38d9-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b38d9-127">Header</span><span class="sxs-lookup"><span data-stu-id="b38d9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b38d9-128"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b38d9-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b38d9-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b38d9-129">Library</span></span><br/> | <dl> <span data-ttu-id="b38d9-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b38d9-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b38d9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b38d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b38d9-132">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="b38d9-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




