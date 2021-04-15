---
description: 'Метод Block блокирует или разблокирует поток данных из ПИН-кода. Этот метод реализует метод Ипинфловконтрол:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Метод Кдинамикаутпутпин. Block (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669429"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="42cd7-104">Метод Кдинамикаутпутпин. Block</span><span class="sxs-lookup"><span data-stu-id="42cd7-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="42cd7-105">`Block`Метод блокирует или разблокирует поток данных из ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="42cd7-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="42cd7-106">Этот метод реализует метод [**ипинфловконтрол:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .</span><span class="sxs-lookup"><span data-stu-id="42cd7-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42cd7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42cd7-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="42cd7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42cd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42cd7-109">*двблоккфлагс*</span><span class="sxs-lookup"><span data-stu-id="42cd7-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="42cd7-110">Флаг, указывающий, следует ли блокировать или разблокировать ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="42cd7-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="42cd7-111">Необходимо установить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="42cd7-111">Must be one of the following values:</span></span>

<span data-ttu-id="42cd7-112">Нуль: разблокировать поток данных из ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="42cd7-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="42cd7-113">\_Закрепление \_ \_ блока управления потоком \_ : Блокировка потока данных из ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="42cd7-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="42cd7-114">*хевент*</span><span class="sxs-lookup"><span data-stu-id="42cd7-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="42cd7-115">Указатель на объект события или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="42cd7-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42cd7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42cd7-116">Return value</span></span>

<span data-ttu-id="42cd7-117">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42cd7-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="42cd7-118">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="42cd7-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="42cd7-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="42cd7-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="42cd7-120">Описание</span><span class="sxs-lookup"><span data-stu-id="42cd7-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="42cd7-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="42cd7-122">ПИН-код уже разблокирован.</span><span class="sxs-lookup"><span data-stu-id="42cd7-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="42cd7-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="42cd7-124">Успешно.</span><span class="sxs-lookup"><span data-stu-id="42cd7-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="42cd7-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="42cd7-126">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="42cd7-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="42cd7-127"><dt>**\_ \_ ПИН-код VFW E \_ уже \_ заблокирован**</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="42cd7-128">ПИН-код уже заблокирован в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="42cd7-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="42cd7-129"><dt>**\_ \_ ПИН-код VFW E \_ уже \_ заблокирован \_ в \_ этом \_ потоке**</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="42cd7-130">ПИН-код уже заблокирован в вызывающем потоке.</span><span class="sxs-lookup"><span data-stu-id="42cd7-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42cd7-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42cd7-131">Remarks</span></span>

<span data-ttu-id="42cd7-132">Дополнительные сведения об этом методе см. в разделе [**ипинфловконтрол:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span><span class="sxs-lookup"><span data-stu-id="42cd7-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="42cd7-133">На внутреннем уровне этот метод вызывает один из следующих защищенных методов:</span><span class="sxs-lookup"><span data-stu-id="42cd7-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="42cd7-134">Block (асинхронный): [ **кдинамикаутпутпин:: асинчронаусблоккаутпутпин**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="42cd7-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="42cd7-135">Block (синхронная): [ **кдинамикаутпутпин:: синчронаусблоккаутпутпин**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="42cd7-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="42cd7-136">Разблокировать: [ **кдинамикаутпутпин:: унблоккаутпутпин**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="42cd7-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="42cd7-137">Разблокировка всегда выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="42cd7-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="42cd7-138">Требования</span><span class="sxs-lookup"><span data-stu-id="42cd7-138">Requirements</span></span>



| <span data-ttu-id="42cd7-139">Требование</span><span class="sxs-lookup"><span data-stu-id="42cd7-139">Requirement</span></span> | <span data-ttu-id="42cd7-140">Значение</span><span class="sxs-lookup"><span data-stu-id="42cd7-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cd7-141">Header</span><span class="sxs-lookup"><span data-stu-id="42cd7-141">Header</span></span><br/>  | <dl> <span data-ttu-id="42cd7-142"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="42cd7-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42cd7-143">Library</span></span><br/> | <dl> <span data-ttu-id="42cd7-144"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="42cd7-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42cd7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42cd7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cd7-146">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="42cd7-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




