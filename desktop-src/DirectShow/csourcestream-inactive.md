---
description: 'Неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен. Этот метод переопределяет метод Кбасепин:: Inactive. Если поток потоковой передачи активен, этот метод останавливает его и ждет выхода из потока.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Ксаурцестреам. Inactive-метод (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688840"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="6ef9a-105">Ксаурцестреам. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="6ef9a-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="6ef9a-106">`Inactive`Метод уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="6ef9a-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="6ef9a-107">Этот метод переопределяет метод [**кбасепин:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="6ef9a-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="6ef9a-108">Если поток потоковой передачи активен, этот метод останавливает его и ждет выхода из потока.</span><span class="sxs-lookup"><span data-stu-id="6ef9a-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef9a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ef9a-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="6ef9a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ef9a-110">Parameters</span></span>

<span data-ttu-id="6ef9a-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6ef9a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ef9a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ef9a-112">Return value</span></span>

<span data-ttu-id="6ef9a-113">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ef9a-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef9a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6ef9a-114">Requirements</span></span>



| <span data-ttu-id="6ef9a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6ef9a-115">Requirement</span></span> | <span data-ttu-id="6ef9a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6ef9a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef9a-117">Header</span><span class="sxs-lookup"><span data-stu-id="6ef9a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6ef9a-118"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef9a-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6ef9a-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ef9a-119">Library</span></span><br/> | <dl> <span data-ttu-id="6ef9a-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef9a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef9a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ef9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef9a-122">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="6ef9a-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




