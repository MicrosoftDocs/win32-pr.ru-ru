---
description: 'Метод Инитиалсреадпрок вызывает метод Каутпуткуеуе:: Среадпрок при создании потока.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Iniметод Тиалсреадпрок (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679702"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="50d4d-103">COutputQueue.Iniметод Тиалсреадпрок</span><span class="sxs-lookup"><span data-stu-id="50d4d-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="50d4d-104">`InitialThreadProc`При создании потока метод вызывает метод [**каутпуткуеуе:: среадпрок**](coutputqueue-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="50d4d-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50d4d-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="50d4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50d4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d4d-107">*PV*</span><span class="sxs-lookup"><span data-stu-id="50d4d-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4d-108">`this` вид.</span><span class="sxs-lookup"><span data-stu-id="50d4d-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d4d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50d4d-109">Return value</span></span>

<span data-ttu-id="50d4d-110">Возвращает значение, возвращаемое методом [**каутпуткуеуе:: среадпрок**](coutputqueue-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="50d4d-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d4d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50d4d-111">Remarks</span></span>

<span data-ttu-id="50d4d-112">Этот метод является процедурой потока для рабочего потока объекта.</span><span class="sxs-lookup"><span data-stu-id="50d4d-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="50d4d-113">`this`Указатель объекта является параметром потока.</span><span class="sxs-lookup"><span data-stu-id="50d4d-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="50d4d-114">Метод отменяет ссылку на него для вызова **среадпрок**.</span><span class="sxs-lookup"><span data-stu-id="50d4d-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="50d4d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="50d4d-115">Requirements</span></span>



| <span data-ttu-id="50d4d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="50d4d-116">Requirement</span></span> | <span data-ttu-id="50d4d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50d4d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d4d-118">Header</span><span class="sxs-lookup"><span data-stu-id="50d4d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="50d4d-119"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50d4d-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50d4d-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50d4d-120">Library</span></span><br/> | <dl> <span data-ttu-id="50d4d-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="50d4d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d4d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50d4d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d4d-123">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="50d4d-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




