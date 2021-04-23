---
description: Метод ДеЦидеаллокатор выбирает распределитель памяти.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Кбасеаутпутпин. ДеЦидеаллокатор, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657517"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="8c3ee-103">Кбасеаутпутпин. ДеЦидеаллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="8c3ee-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="8c3ee-104">`DecideAllocator`Метод выбирает распределитель памяти.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c3ee-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="8c3ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c3ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3ee-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="8c3ee-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="8c3ee-108">Указатель на интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8c3ee-109">*паллок*</span><span class="sxs-lookup"><span data-stu-id="8c3ee-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="8c3ee-110">Адрес переменной, которая получает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3ee-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c3ee-111">Return value</span></span>

<span data-ttu-id="8c3ee-112">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c3ee-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c3ee-113">Remarks</span></span>

<span data-ttu-id="8c3ee-114">Этот метод вызывается в конце процесса подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="8c3ee-115">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8c3ee-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="8c3ee-116">Вызывает метод [**имеминпутпин:: жеталлокаторрекуирементс**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) , чтобы получить требования к буферу входного контакта, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="8c3ee-117">Вызывает метод [**имеминпутпин::-распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) для запроса распределителя от входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="8c3ee-118">Если входной ПИН-код не предоставляет распределителя, то закрепление вывода создает его путем вызова метода класса [**кбасеаутпутпин:: иниталлокатор**](cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="8c3ee-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="8c3ee-119">Вызывает метод класса [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md) , который задает свойства распределителя.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="8c3ee-120">Это чистый виртуальный метод; производный класс должен реализовать его.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="8c3ee-121">Вызывает метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , который уведомляет входной ПИН-код распределителя, который используется.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3ee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8c3ee-122">Requirements</span></span>



| <span data-ttu-id="8c3ee-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8c3ee-123">Requirement</span></span> | <span data-ttu-id="8c3ee-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8c3ee-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3ee-125">Header</span><span class="sxs-lookup"><span data-stu-id="8c3ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8c3ee-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c3ee-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8c3ee-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c3ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="8c3ee-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8c3ee-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c3ee-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c3ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3ee-130">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="8c3ee-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




