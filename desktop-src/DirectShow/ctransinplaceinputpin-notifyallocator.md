---
description: 'Метод Нотифяллокатор задает распределитель для соединения. Этот метод реализует метод Имеминпутпин:: Нотифяллокатор.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Ктрансинплацеинпутпин. Нотифяллокатор, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657082"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="3444c-104">Ктрансинплацеинпутпин. Нотифяллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="3444c-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="3444c-105">`NotifyAllocator`Метод задает распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="3444c-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="3444c-106">Этот метод реализует метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="3444c-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3444c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3444c-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="3444c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3444c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3444c-109">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="3444c-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="3444c-110">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="3444c-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3444c-111">*бреадонли*</span><span class="sxs-lookup"><span data-stu-id="3444c-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="3444c-112">Флаг, указывающий, доступны ли образцы из этого распределителя только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3444c-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="3444c-113">Если **значение — true**, образцы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3444c-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3444c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3444c-114">Return value</span></span>

<span data-ttu-id="3444c-115">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3444c-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3444c-116">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3444c-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="3444c-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3444c-117">Return code</span></span>                                                                               | <span data-ttu-id="3444c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3444c-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="3444c-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3444c-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3444c-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="3444c-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="3444c-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="3444c-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="3444c-122">Failure</span><span class="sxs-lookup"><span data-stu-id="3444c-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="3444c-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="3444c-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3444c-124">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="3444c-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3444c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3444c-125">Remarks</span></span>

<span data-ttu-id="3444c-126">Фильтр пытается использовать один и тот же распределитель для обоих подключений.</span><span class="sxs-lookup"><span data-stu-id="3444c-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="3444c-127">Если выходной ПИН-код не подключен, входной ПИН-код автоматически принимает распределитель.</span><span class="sxs-lookup"><span data-stu-id="3444c-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="3444c-128">Когда выходной ПИН-код подключен, фильтр повторно подключает входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3444c-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="3444c-129">На этом этапе фильтр повторит попытку использования одного распределителя.</span><span class="sxs-lookup"><span data-stu-id="3444c-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="3444c-130">Если выходной ПИН-код подключен, то входной ПИН-код принимает распределитель.</span><span class="sxs-lookup"><span data-stu-id="3444c-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="3444c-131">Закрепление вывода также использует тот же распределитель.</span><span class="sxs-lookup"><span data-stu-id="3444c-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="3444c-132">Он вызывает `NotifyAllocator` для входного ПИН-кода нисходящего.</span><span class="sxs-lookup"><span data-stu-id="3444c-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="3444c-133">В предыдущем случае возникло следующее исключение:</span><span class="sxs-lookup"><span data-stu-id="3444c-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="3444c-134">Если предложенный распределитель доступен только для чтения (то есть параметр *бреадонли* имеет **значение true**), а фильтру необходимо изменить образцы, то фильтр должен использовать два разных распределителя.</span><span class="sxs-lookup"><span data-stu-id="3444c-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="3444c-135">В этом случае, если вышестоящий фильтр предлагает использовать распределитель подчиненного фильтра, метод возвращает значение E \_ Failed.</span><span class="sxs-lookup"><span data-stu-id="3444c-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3444c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3444c-136">Requirements</span></span>



| <span data-ttu-id="3444c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3444c-137">Requirement</span></span> | <span data-ttu-id="3444c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3444c-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3444c-139">Header</span><span class="sxs-lookup"><span data-stu-id="3444c-139">Header</span></span><br/>  | <dl> <span data-ttu-id="3444c-140"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3444c-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3444c-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3444c-141">Library</span></span><br/> | <dl> <span data-ttu-id="3444c-142"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3444c-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3444c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3444c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3444c-144">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="3444c-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




