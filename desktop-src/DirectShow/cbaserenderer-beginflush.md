---
description: Кбасерендерер. Бегинфлуш, метод Бегинфлуш начинает операцию очистки.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Кбасерендерер. Бегинфлуш, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095942"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="0dcb0-103">Кбасерендерер. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="0dcb0-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="0dcb0-104">`BeginFlush`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="0dcb0-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dcb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dcb0-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="0dcb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dcb0-106">Parameters</span></span>

<span data-ttu-id="0dcb0-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0dcb0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dcb0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dcb0-108">Return value</span></span>

<span data-ttu-id="0dcb0-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0dcb0-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dcb0-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="0dcb0-110">Remarks</span></span>

<span data-ttu-id="0dcb0-111">Входной ПИН-код фильтра вызывает этот метод при получении вызова метода [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="0dcb0-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="0dcb0-112">Фильтр освобождает поток потоковой передачи и освобождает все примеры, которые он удерживает для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0dcb0-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dcb0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0dcb0-113">Requirements</span></span>



| <span data-ttu-id="0dcb0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0dcb0-114">Requirement</span></span> | <span data-ttu-id="0dcb0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0dcb0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dcb0-116">Header</span><span class="sxs-lookup"><span data-stu-id="0dcb0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0dcb0-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dcb0-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0dcb0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0dcb0-118">Library</span></span><br/> | <dl> <span data-ttu-id="0dcb0-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0dcb0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dcb0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0dcb0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dcb0-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="0dcb0-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




