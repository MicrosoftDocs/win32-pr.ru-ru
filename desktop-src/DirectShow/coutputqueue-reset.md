---
description: Метод Reset сбрасывает объект, чтобы он мог получить больше данных.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Метод Каутпуткуеуе. Reset (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674879"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="2f00f-103">Каутпуткуеуе. Reset, метод</span><span class="sxs-lookup"><span data-stu-id="2f00f-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="2f00f-104">`Reset`Метод сбрасывает объект, чтобы он мог получить больше данных.</span><span class="sxs-lookup"><span data-stu-id="2f00f-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f00f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f00f-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="2f00f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f00f-106">Parameters</span></span>

<span data-ttu-id="2f00f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2f00f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f00f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f00f-108">Return value</span></span>

<span data-ttu-id="2f00f-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2f00f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f00f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f00f-110">Remarks</span></span>

<span data-ttu-id="2f00f-111">Этот метод сбрасывает переменную члена [**каутпуткуеуе:: m \_ HR**](coutputqueue-m-hr.md) в значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2f00f-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="2f00f-112">Объект может снова получать примеры мультимедиа; Например, после операции очистки.</span><span class="sxs-lookup"><span data-stu-id="2f00f-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f00f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2f00f-113">Requirements</span></span>



| <span data-ttu-id="2f00f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2f00f-114">Requirement</span></span> | <span data-ttu-id="2f00f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2f00f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f00f-116">Header</span><span class="sxs-lookup"><span data-stu-id="2f00f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2f00f-117"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f00f-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f00f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f00f-118">Library</span></span><br/> | <dl> <span data-ttu-id="2f00f-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2f00f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f00f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f00f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f00f-121">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="2f00f-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




