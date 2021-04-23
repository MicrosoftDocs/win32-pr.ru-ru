---
description: Метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Кбасеаутпутпин. Бреакконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657521"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="28aab-103">Кбасеаутпутпин. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="28aab-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="28aab-104">`BreakConnect`Метод освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="28aab-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="28aab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28aab-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="28aab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28aab-106">Parameters</span></span>

<span data-ttu-id="28aab-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="28aab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28aab-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28aab-108">Return value</span></span>

<span data-ttu-id="28aab-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="28aab-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="28aab-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28aab-110">Remarks</span></span>

<span data-ttu-id="28aab-111">Этот метод переопределяет метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="28aab-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="28aab-112">Он снимает распределитель и освобождает интерфейсы [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) и [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="28aab-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="28aab-113">При переопределении этого метода вызовите метод базового класса из переопределяющего метода.</span><span class="sxs-lookup"><span data-stu-id="28aab-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="28aab-114">В противном случае могут возникнуть утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="28aab-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="28aab-115">Требования</span><span class="sxs-lookup"><span data-stu-id="28aab-115">Requirements</span></span>



| <span data-ttu-id="28aab-116">Требование</span><span class="sxs-lookup"><span data-stu-id="28aab-116">Requirement</span></span> | <span data-ttu-id="28aab-117">Значение</span><span class="sxs-lookup"><span data-stu-id="28aab-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28aab-118">Header</span><span class="sxs-lookup"><span data-stu-id="28aab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="28aab-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28aab-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="28aab-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28aab-120">Library</span></span><br/> | <dl> <span data-ttu-id="28aab-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="28aab-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28aab-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28aab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28aab-123">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="28aab-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




