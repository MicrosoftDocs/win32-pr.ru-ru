---
description: Кбасепин. Комплетеконнект, метод Комплетеконнект завершает подключение к другому ПИН-коду.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Кбасепин. Комплетеконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096042"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="13949-103">Кбасепин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="13949-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="13949-104">`CompleteConnect`Метод завершает подключение к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="13949-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="13949-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13949-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="13949-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13949-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="13949-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="13949-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="13949-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13949-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13949-109">Return value</span></span>

<span data-ttu-id="13949-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="13949-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="13949-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="13949-111">Remarks</span></span>

<span data-ttu-id="13949-112">Этот метод вызывается на обоих ПИН-кодах в конце процесса подключения.</span><span class="sxs-lookup"><span data-stu-id="13949-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="13949-113">Соединительный ПИН-код вызывает его в методе [**кбасепин:: Connect**](cbasepin-connect.md) , а принимающий ПИН-код вызывает его из метода [**Кбасепин:: рецеивеконнектион**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="13949-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="13949-114">В базовом классе этот метод просто возвращает значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="13949-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="13949-115">Если производный класс имеет какие-либо требования для завершения соединения, он должен переопределить этот метод.</span><span class="sxs-lookup"><span data-stu-id="13949-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="13949-116">Например, класс [**кбасеаутпутпин**](cbaseoutputpin.md) использует этот метод для выбора распределителя памяти.</span><span class="sxs-lookup"><span data-stu-id="13949-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="13949-117">Если этот метод завершается неудачно, Общая попытка подключения также завершается сбоем, а ПИН-код отключается от полученного PIN-кода.</span><span class="sxs-lookup"><span data-stu-id="13949-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="13949-118">Требования</span><span class="sxs-lookup"><span data-stu-id="13949-118">Requirements</span></span>



| <span data-ttu-id="13949-119">Требование</span><span class="sxs-lookup"><span data-stu-id="13949-119">Requirement</span></span> | <span data-ttu-id="13949-120">Значение</span><span class="sxs-lookup"><span data-stu-id="13949-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13949-121">Header</span><span class="sxs-lookup"><span data-stu-id="13949-121">Header</span></span><br/>  | <dl> <span data-ttu-id="13949-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13949-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="13949-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13949-123">Library</span></span><br/> | <dl> <span data-ttu-id="13949-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="13949-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13949-125">См. также</span><span class="sxs-lookup"><span data-stu-id="13949-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13949-126">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="13949-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




