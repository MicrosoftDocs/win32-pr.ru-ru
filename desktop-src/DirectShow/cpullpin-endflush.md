---
description: Метод Ендфлуш информирует фильтр владельца о завершении операции очистки. Производный класс должен реализовывать этот метод.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Кпуллпин. Ендфлуш, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669057"
---
# <a name="cpullpinendflush-method"></a><span data-ttu-id="d00f6-104">Кпуллпин. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="d00f6-104">CPullPin.EndFlush method</span></span>

<span data-ttu-id="d00f6-105">`EndFlush`Метод информирует фильтр владельца о завершении операции очистки.</span><span class="sxs-lookup"><span data-stu-id="d00f6-105">The `EndFlush` method informs the owning filter to end a flush operation.</span></span> <span data-ttu-id="d00f6-106">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="d00f6-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d00f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d00f6-107">Syntax</span></span>


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a><span data-ttu-id="d00f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d00f6-108">Parameters</span></span>

<span data-ttu-id="d00f6-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d00f6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d00f6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d00f6-110">Return value</span></span>

<span data-ttu-id="d00f6-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d00f6-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d00f6-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d00f6-112">Remarks</span></span>

<span data-ttu-id="d00f6-113">Метод [**кпуллпин:: Seek**](cpullpin-seek.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="d00f6-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="d00f6-114">Реализуйте этот метод, чтобы вызвать метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для каждого нисходящиго входного ПИН-кода, получающего данные от этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d00f6-114">Implement this method to call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="d00f6-115">Если закрепление вывода фильтра является производным от **кбасеаутпутпин**, вызовите метод **Кбасеаутпутпин::D еливерендфлуш** .</span><span class="sxs-lookup"><span data-stu-id="d00f6-115">If your filter's output pin(s) derive from **CBaseOutputPin**, call the **CBaseOutputPin::DeliverEndFlush** method.</span></span>

<span data-ttu-id="d00f6-116">Такая схема позволяет фильтровать поиск в потоке, просто вызывая метод **Seek** для объекта **кпуллпин** .</span><span class="sxs-lookup"><span data-stu-id="d00f6-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00f6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d00f6-117">Requirements</span></span>



| <span data-ttu-id="d00f6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d00f6-118">Requirement</span></span> | <span data-ttu-id="d00f6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d00f6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d00f6-120">Header</span><span class="sxs-lookup"><span data-stu-id="d00f6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d00f6-121"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="d00f6-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="d00f6-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d00f6-122">Library</span></span><br/> | <dl> <span data-ttu-id="d00f6-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d00f6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00f6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d00f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00f6-125">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="d00f6-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




