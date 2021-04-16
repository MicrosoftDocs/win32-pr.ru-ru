---
description: Метод Connect завершает соединение с выходным закреплением.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Метод Кпуллпин. Connect (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679654"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="55395-103">Кпуллпин. Connect, метод</span><span class="sxs-lookup"><span data-stu-id="55395-103">CPullPin.Connect method</span></span>

<span data-ttu-id="55395-104">`Connect`Метод завершает соединение с выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="55395-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="55395-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55395-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="55395-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55395-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="55395-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="55395-108">Указатель на интерфейс **IUnknown** выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="55395-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="55395-109">*паллок*</span><span class="sxs-lookup"><span data-stu-id="55395-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="55395-110">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) предпочтительного распределителя входного контакта или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="55395-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="55395-111">*бсинк*</span><span class="sxs-lookup"><span data-stu-id="55395-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="55395-112">Логическое значение, указывающее, следует ли использовать синхронные операции чтения.</span><span class="sxs-lookup"><span data-stu-id="55395-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="55395-113">Если **значение — true**, ПИН-код выполняет синхронные операции чтения для выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="55395-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="55395-114">Если **значение равно false**, то ПИН-код выполняет асинхронные запросы на чтение.</span><span class="sxs-lookup"><span data-stu-id="55395-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55395-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55395-115">Return value</span></span>

<span data-ttu-id="55395-116">Возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="55395-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="55395-117">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="55395-117">Possible values include the following.</span></span>



| <span data-ttu-id="55395-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="55395-118">Return code</span></span>                                                                                               | <span data-ttu-id="55395-119">Описание</span><span class="sxs-lookup"><span data-stu-id="55395-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55395-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="55395-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="55395-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="55395-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="55395-122"><dt>**VFW \_ E \_ уже \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="55395-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="55395-123">Входной ПИН-код уже подключен.</span><span class="sxs-lookup"><span data-stu-id="55395-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="55395-124"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="55395-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="55395-125">Закрепление вывода не предоставляет [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span><span class="sxs-lookup"><span data-stu-id="55395-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55395-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55395-126">Remarks</span></span>

<span data-ttu-id="55395-127">Вызывайте этот метод во время подключения входного контакта.</span><span class="sxs-lookup"><span data-stu-id="55395-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="55395-128">Если метод завершается сбоем, ПИН-код не должен подключиться.</span><span class="sxs-lookup"><span data-stu-id="55395-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="55395-129">Этот метод запрашивает выходной ПИН-код для интерфейса **иасинкреадер** .</span><span class="sxs-lookup"><span data-stu-id="55395-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="55395-130">В случае успеха вызывается [**кпуллпин::D еЦидеаллокатор**](cpullpin-decideallocator.md) для согласования распределителя для подключения.</span><span class="sxs-lookup"><span data-stu-id="55395-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="55395-131">Если входной ПИН-код имеет предпочтительный распределитель, укажите его в параметре *паллок* . метод **деЦидеаллокатор** передает этот указатель в метод [**Иасинкреадер:: рекуесталлокатор**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="55395-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="55395-132">В противном случае установите для *Паллок* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="55395-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="55395-133">Если значение *бсинк* равно **true**, то объект **кпуллпин** выполняет синхронные запросы чтения путем вызова [**иасинкреадер:: синкреадалигнед**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="55395-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="55395-134">В противном случае вызывается метод [**иасинкреадер:: request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) для выполнения перекрывающихся запросов на чтение.</span><span class="sxs-lookup"><span data-stu-id="55395-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="55395-135">Требования</span><span class="sxs-lookup"><span data-stu-id="55395-135">Requirements</span></span>



| <span data-ttu-id="55395-136">Требование</span><span class="sxs-lookup"><span data-stu-id="55395-136">Requirement</span></span> | <span data-ttu-id="55395-137">Значение</span><span class="sxs-lookup"><span data-stu-id="55395-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55395-138">Header</span><span class="sxs-lookup"><span data-stu-id="55395-138">Header</span></span><br/>  | <dl> <span data-ttu-id="55395-139"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="55395-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="55395-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55395-140">Library</span></span><br/> | <dl> <span data-ttu-id="55395-141"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="55395-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55395-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55395-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55395-143">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="55395-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




