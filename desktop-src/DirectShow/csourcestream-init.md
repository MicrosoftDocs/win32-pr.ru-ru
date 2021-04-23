---
description: Метод init инициализирует поток потоковой передачи.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Метод CSourceStream.Init (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689016"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="da683-103">Метод CSourceStream.Init</span><span class="sxs-lookup"><span data-stu-id="da683-103">CSourceStream.Init method</span></span>

<span data-ttu-id="da683-104">`Init`Метод инициализирует поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="da683-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="da683-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da683-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="da683-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da683-106">Parameters</span></span>

<span data-ttu-id="da683-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="da683-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da683-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da683-108">Return value</span></span>

<span data-ttu-id="da683-109">Возвращает \_ или другое значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da683-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da683-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da683-110">Remarks</span></span>

<span data-ttu-id="da683-111">Этот метод должен быть первым запросом потока, отправленным методу [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="da683-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="da683-112">Метод [**ксаурцестреам:: Active**](csourcestream-active.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="da683-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="da683-113">Требования</span><span class="sxs-lookup"><span data-stu-id="da683-113">Requirements</span></span>



| <span data-ttu-id="da683-114">Требование</span><span class="sxs-lookup"><span data-stu-id="da683-114">Requirement</span></span> | <span data-ttu-id="da683-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da683-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da683-116">Header</span><span class="sxs-lookup"><span data-stu-id="da683-116">Header</span></span><br/>  | <dl> <span data-ttu-id="da683-117"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da683-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="da683-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da683-118">Library</span></span><br/> | <dl> <span data-ttu-id="da683-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="da683-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da683-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da683-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da683-121">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="da683-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




