---
description: 'Кбасеинпутпин. Нотифяллокатор, метод Нотифяллокатор задает распределитель для соединения. Этот метод реализует метод Имеминпутпин:: Нотифяллокатор.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Кбасеинпутпин. Нотифяллокатор, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099719"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="6cc76-104">Кбасеинпутпин. Нотифяллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="6cc76-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="6cc76-105">`NotifyAllocator`Метод задает распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="6cc76-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="6cc76-106">Этот метод реализует метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="6cc76-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc76-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cc76-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="6cc76-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cc76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc76-109">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="6cc76-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc76-110">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="6cc76-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6cc76-111">*бреадонли*</span><span class="sxs-lookup"><span data-stu-id="6cc76-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc76-112">Флаг, указывающий, доступны ли образцы из этого распределителя только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc76-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="6cc76-113">Если **значение — true**, образцы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc76-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc76-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cc76-114">Return value</span></span>

<span data-ttu-id="6cc76-115">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6cc76-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc76-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="6cc76-116">Remarks</span></span>

<span data-ttu-id="6cc76-117">Во время соединения с закреплением выходной ПИН-код выбирает распределитель и вызывает этот метод, чтобы уведомить входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="6cc76-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="6cc76-118">Закрепление вывода может использовать распределитель, предложенный входным закреплением в методе [**имеминпутпин::-распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) , или предоставить собственный распределитель.</span><span class="sxs-lookup"><span data-stu-id="6cc76-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc76-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6cc76-119">Requirements</span></span>



| <span data-ttu-id="6cc76-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6cc76-120">Requirement</span></span> | <span data-ttu-id="6cc76-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6cc76-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc76-122">Header</span><span class="sxs-lookup"><span data-stu-id="6cc76-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6cc76-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cc76-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6cc76-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6cc76-124">Library</span></span><br/> | <dl> <span data-ttu-id="6cc76-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6cc76-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc76-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6cc76-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc76-127">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="6cc76-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




