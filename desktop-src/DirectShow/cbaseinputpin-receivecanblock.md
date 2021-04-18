---
description: 'Метод Рецеивеканблокк определяет, могут ли вызовы метода Имеминпутпин:: Receive блокироваться. Этот метод реализует метод Имеминпутпин:: Рецеивеканблокк.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Кбасеинпутпин. Рецеивеканблокк, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658025"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="fab20-104">Кбасеинпутпин. Рецеивеканблокк, метод</span><span class="sxs-lookup"><span data-stu-id="fab20-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="fab20-105">`ReceiveCanBlock`Метод определяет, могут ли вызовы метода [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) блокироваться.</span><span class="sxs-lookup"><span data-stu-id="fab20-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="fab20-106">Этот метод реализует метод [**имеминпутпин:: рецеивеканблокк**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .</span><span class="sxs-lookup"><span data-stu-id="fab20-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab20-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fab20-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="fab20-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fab20-108">Parameters</span></span>

<span data-ttu-id="fab20-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fab20-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fab20-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fab20-110">Return value</span></span>

<span data-ttu-id="fab20-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fab20-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fab20-112">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fab20-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="fab20-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fab20-113">Return code</span></span>                                                                             | <span data-ttu-id="fab20-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fab20-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="fab20-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fab20-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="fab20-116">ПИН-код не будет блокироваться при вызове метода **Receive**.</span><span class="sxs-lookup"><span data-stu-id="fab20-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="fab20-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fab20-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="fab20-118">ПИН-код может блокироваться при вызове метода **Receive**.</span><span class="sxs-lookup"><span data-stu-id="fab20-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="fab20-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fab20-119">Remarks</span></span>

<span data-ttu-id="fab20-120">Возвращает \_ значение false, если вызовы метода **Receive** гарантированно не блокируются.</span><span class="sxs-lookup"><span data-stu-id="fab20-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="fab20-121">В противном случае возвратите значение S \_ OK или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="fab20-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="fab20-122">Если метод **Receive** вызывает **Получение** по нисходящему ПИН-коду, то он может блокироваться; `ReceiveCanBlock` необходимо учитывать этот фактор.</span><span class="sxs-lookup"><span data-stu-id="fab20-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="fab20-123">Вышестоящий фильтр может использовать этот метод для определения своей стратегии работы с потоками.</span><span class="sxs-lookup"><span data-stu-id="fab20-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="fab20-124">Если метод **Receive** может блокироваться, вышестоящий фильтр может принять решение использовать рабочий поток, который помещает данные в буфер.</span><span class="sxs-lookup"><span data-stu-id="fab20-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="fab20-125">Реализация этой стратегии приведена в описании класса [**каутпуткуеуе**](coutputqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="fab20-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="fab20-126">В базовом классе этот метод возвращает \_ значение ОК, если выполняется любое из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="fab20-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="fab20-127">Фильтр не имеет выходных закрепления.</span><span class="sxs-lookup"><span data-stu-id="fab20-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="fab20-128">Входной ПИН-код, подключенный к этому фильтру, сигнализирует, что он может блокироваться.</span><span class="sxs-lookup"><span data-stu-id="fab20-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="fab20-129">Входной ПИН-код, подключенный к этому фильтру, не поддерживает интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="fab20-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab20-130">Требования</span><span class="sxs-lookup"><span data-stu-id="fab20-130">Requirements</span></span>



| <span data-ttu-id="fab20-131">Требование</span><span class="sxs-lookup"><span data-stu-id="fab20-131">Requirement</span></span> | <span data-ttu-id="fab20-132">Значение</span><span class="sxs-lookup"><span data-stu-id="fab20-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab20-133">Header</span><span class="sxs-lookup"><span data-stu-id="fab20-133">Header</span></span><br/>  | <dl> <span data-ttu-id="fab20-134"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fab20-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fab20-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fab20-135">Library</span></span><br/> | <dl> <span data-ttu-id="fab20-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fab20-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab20-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fab20-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab20-138">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="fab20-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




