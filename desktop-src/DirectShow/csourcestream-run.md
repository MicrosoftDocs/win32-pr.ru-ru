---
description: Метод Run сообщает поток потоковой передачи для выполнения.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Метод Ксаурцестреам. Run (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679828"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="87d2f-103">Ксаурцестреам. Run, метод</span><span class="sxs-lookup"><span data-stu-id="87d2f-103">CSourceStream.Run method</span></span>

<span data-ttu-id="87d2f-104">`Run`Метод оповещает поток потоковой передачи о выполнении.</span><span class="sxs-lookup"><span data-stu-id="87d2f-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87d2f-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="87d2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87d2f-106">Parameters</span></span>

<span data-ttu-id="87d2f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="87d2f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87d2f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87d2f-108">Return value</span></span>

<span data-ttu-id="87d2f-109">Непредвиденное значение: S \_ (ОК или E) \_ .</span><span class="sxs-lookup"><span data-stu-id="87d2f-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d2f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87d2f-110">Remarks</span></span>

<span data-ttu-id="87d2f-111">В базовом классе этот метод действует так же, как запрос [**ксаурцестреам::P Аусе**](csourcestream-pause.md) , и не используется.</span><span class="sxs-lookup"><span data-stu-id="87d2f-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d2f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="87d2f-112">Requirements</span></span>



| <span data-ttu-id="87d2f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="87d2f-113">Requirement</span></span> | <span data-ttu-id="87d2f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="87d2f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d2f-115">Header</span><span class="sxs-lookup"><span data-stu-id="87d2f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="87d2f-116"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87d2f-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="87d2f-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87d2f-117">Library</span></span><br/> | <dl> <span data-ttu-id="87d2f-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="87d2f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d2f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87d2f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d2f-120">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="87d2f-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




