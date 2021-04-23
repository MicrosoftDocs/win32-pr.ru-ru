---
description: Метод Онсреаддестрой вызывается, когда поток потоковой передачи собирается завершить работу.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Метод Ксаурцестреам. Онсреаддестрой (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657623"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="e2700-103">Ксаурцестреам. Онсреаддестрой, метод</span><span class="sxs-lookup"><span data-stu-id="e2700-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="e2700-104">`OnThreadDestroy`Метод вызывается, когда поток потоковой передачи собирается завершить работу.</span><span class="sxs-lookup"><span data-stu-id="e2700-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2700-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2700-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="e2700-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2700-106">Parameters</span></span>

<span data-ttu-id="e2700-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e2700-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2700-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2700-108">Return value</span></span>

<span data-ttu-id="e2700-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e2700-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2700-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2700-110">Remarks</span></span>

<span data-ttu-id="e2700-111">Процедура потока, [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md), вызывает этот метод перед выходом.</span><span class="sxs-lookup"><span data-stu-id="e2700-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="e2700-112">Метод не выполняет никаких действий в базовом классе. Он доступен для переопределения производного класса.</span><span class="sxs-lookup"><span data-stu-id="e2700-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="e2700-113">Если производный класс возвращает код ошибки, то поток завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e2700-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2700-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e2700-114">Requirements</span></span>



| <span data-ttu-id="e2700-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e2700-115">Requirement</span></span> | <span data-ttu-id="e2700-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e2700-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2700-117">Header</span><span class="sxs-lookup"><span data-stu-id="e2700-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e2700-118"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2700-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e2700-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e2700-119">Library</span></span><br/> | <dl> <span data-ttu-id="e2700-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e2700-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2700-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2700-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2700-122">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="e2700-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




