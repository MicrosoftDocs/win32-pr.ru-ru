---
description: Метод деструктора Ксаурцестреам. ~ Ксаурцестреам.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Деструктор Ксаурцестреам. ~ Ксаурцестреам (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085212"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="025e6-103">Деструктор Ксаурцестреам. ~ Ксаурцестреам</span><span class="sxs-lookup"><span data-stu-id="025e6-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="025e6-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="025e6-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="025e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="025e6-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="025e6-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="025e6-106">Remarks</span></span>

<span data-ttu-id="025e6-107">Деструктор автоматически удаляет ПИН-код из фильтра владельца, вызывая [**ксаурце:: ремовепин**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="025e6-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="025e6-108">Требования</span><span class="sxs-lookup"><span data-stu-id="025e6-108">Requirements</span></span>



| <span data-ttu-id="025e6-109">Требование</span><span class="sxs-lookup"><span data-stu-id="025e6-109">Requirement</span></span> | <span data-ttu-id="025e6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="025e6-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="025e6-111">Header</span><span class="sxs-lookup"><span data-stu-id="025e6-111">Header</span></span><br/>  | <dl> <span data-ttu-id="025e6-112"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="025e6-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="025e6-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="025e6-113">Library</span></span><br/> | <dl> <span data-ttu-id="025e6-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="025e6-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="025e6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="025e6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="025e6-116">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="025e6-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




