---
description: Метод «завершение» сигнализирует потоку потоковой передачи на завершение.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Метод Ксаурцестреам. останавливаться (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675405"
---
# <a name="csourcestreamstop-method"></a><span data-ttu-id="44566-103">Ксаурцестреам. останавливаться, метод</span><span class="sxs-lookup"><span data-stu-id="44566-103">CSourceStream.Stop method</span></span>

<span data-ttu-id="44566-104">`Stop`Метод сигнализирует потоку потоковой передачи на завершение.</span><span class="sxs-lookup"><span data-stu-id="44566-104">The `Stop` method signals the streaming thread to stop.</span></span>

## <a name="syntax"></a><span data-ttu-id="44566-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44566-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="44566-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44566-106">Parameters</span></span>

<span data-ttu-id="44566-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="44566-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44566-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44566-108">Return value</span></span>

<span data-ttu-id="44566-109">Непредвиденное значение: S \_ (ОК или E) \_ .</span><span class="sxs-lookup"><span data-stu-id="44566-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="44566-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44566-110">Remarks</span></span>

<span data-ttu-id="44566-111">Метод [**ксаурцестреам:: Inactive**](csourcestream-inactive.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="44566-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="44566-112">Требования</span><span class="sxs-lookup"><span data-stu-id="44566-112">Requirements</span></span>



| <span data-ttu-id="44566-113">Требование</span><span class="sxs-lookup"><span data-stu-id="44566-113">Requirement</span></span> | <span data-ttu-id="44566-114">Значение</span><span class="sxs-lookup"><span data-stu-id="44566-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44566-115">Header</span><span class="sxs-lookup"><span data-stu-id="44566-115">Header</span></span><br/>  | <dl> <span data-ttu-id="44566-116"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44566-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="44566-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44566-117">Library</span></span><br/> | <dl> <span data-ttu-id="44566-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="44566-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44566-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44566-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44566-120">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="44566-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




