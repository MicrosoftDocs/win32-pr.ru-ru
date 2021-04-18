---
description: Метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Кбасеинпутпин. Бреакконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6981ef97b98cc25b1996f1599d6d66b8e7d41f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657294"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="fad55-103">Кбасеинпутпин. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="fad55-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="fad55-104">`BreakConnect`Метод освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="fad55-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fad55-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="fad55-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fad55-106">Parameters</span></span>

<span data-ttu-id="fad55-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fad55-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fad55-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fad55-108">Return value</span></span>

<span data-ttu-id="fad55-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="fad55-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad55-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fad55-110">Remarks</span></span>

<span data-ttu-id="fad55-111">Этот метод переопределяет метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="fad55-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="fad55-112">Он снимает распределитель и освобождает интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="fad55-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="fad55-113">При переопределении этого метода вызовите метод базового класса из переопределяющего метода.</span><span class="sxs-lookup"><span data-stu-id="fad55-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="fad55-114">В противном случае могут возникнуть утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="fad55-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad55-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fad55-115">Requirements</span></span>



| <span data-ttu-id="fad55-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fad55-116">Requirement</span></span> | <span data-ttu-id="fad55-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fad55-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fad55-118">Header</span><span class="sxs-lookup"><span data-stu-id="fad55-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fad55-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fad55-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fad55-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fad55-120">Library</span></span><br/> | <dl> <span data-ttu-id="fad55-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fad55-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad55-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fad55-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad55-123">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="fad55-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




