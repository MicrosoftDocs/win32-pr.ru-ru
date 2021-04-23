---
description: Метод Онсреадстартплай вызывается в начале метода Ксаурцестреам::D Обуфферпроцессинглуп.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Метод Ксаурцестреам. Онсреадстартплай (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689014"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="29821-103">Ксаурцестреам. Онсреадстартплай, метод</span><span class="sxs-lookup"><span data-stu-id="29821-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="29821-104">`OnThreadStartPlay`Метод вызывается в начале метода [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="29821-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29821-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29821-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="29821-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29821-106">Parameters</span></span>

<span data-ttu-id="29821-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="29821-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29821-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29821-108">Return value</span></span>

<span data-ttu-id="29821-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="29821-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="29821-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29821-110">Remarks</span></span>

<span data-ttu-id="29821-111">Этот метод не выполняет никаких действий в базовом классе. Он доступен для переопределения производного класса.</span><span class="sxs-lookup"><span data-stu-id="29821-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="29821-112">Требования</span><span class="sxs-lookup"><span data-stu-id="29821-112">Requirements</span></span>



| <span data-ttu-id="29821-113">Требование</span><span class="sxs-lookup"><span data-stu-id="29821-113">Requirement</span></span> | <span data-ttu-id="29821-114">Значение</span><span class="sxs-lookup"><span data-stu-id="29821-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29821-115">Header</span><span class="sxs-lookup"><span data-stu-id="29821-115">Header</span></span><br/>  | <dl> <span data-ttu-id="29821-116"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29821-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="29821-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="29821-117">Library</span></span><br/> | <dl> <span data-ttu-id="29821-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="29821-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29821-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29821-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29821-120">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="29821-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




