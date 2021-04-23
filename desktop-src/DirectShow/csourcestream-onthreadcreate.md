---
description: Метод Онсреадкреате вызывается при инициализации потока потоковой передачи.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Метод Ксаурцестреам. Онсреадкреате (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657624"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="e1f03-103">Ксаурцестреам. Онсреадкреате, метод</span><span class="sxs-lookup"><span data-stu-id="e1f03-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="e1f03-104">`OnThreadCreate`Метод вызывается при инициализации потока потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e1f03-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f03-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1f03-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="e1f03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1f03-106">Parameters</span></span>

<span data-ttu-id="e1f03-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e1f03-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1f03-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1f03-108">Return value</span></span>

<span data-ttu-id="e1f03-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e1f03-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f03-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1f03-110">Remarks</span></span>

<span data-ttu-id="e1f03-111">Процедура потока, [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md), вызывает этот метод при первом получении запроса [**Ксаурцестреам:: init**](csourcestream-init.md) .</span><span class="sxs-lookup"><span data-stu-id="e1f03-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="e1f03-112">Метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="e1f03-112">The method does nothing in the base class.</span></span> <span data-ttu-id="e1f03-113">Производный класс может переопределить этот метод для выполнения инициализации потока.</span><span class="sxs-lookup"><span data-stu-id="e1f03-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="e1f03-114">Если производный класс возвращает код ошибки, то поток завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e1f03-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f03-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e1f03-115">Requirements</span></span>



| <span data-ttu-id="e1f03-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e1f03-116">Requirement</span></span> | <span data-ttu-id="e1f03-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e1f03-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f03-118">Header</span><span class="sxs-lookup"><span data-stu-id="e1f03-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e1f03-119"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f03-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e1f03-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1f03-120">Library</span></span><br/> | <dl> <span data-ttu-id="e1f03-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f03-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f03-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1f03-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f03-123">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="e1f03-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




