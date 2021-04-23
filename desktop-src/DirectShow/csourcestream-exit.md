---
description: Метод Exit сигнализирует потоку потоковой передачи о выходе.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Метод Ксаурцестреам. Exit (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657465"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="2b074-103">Ксаурцестреам. Exit, метод</span><span class="sxs-lookup"><span data-stu-id="2b074-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="2b074-104">`Exit`Метод сообщает потоку потоковой передачи о выходе.</span><span class="sxs-lookup"><span data-stu-id="2b074-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b074-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b074-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="2b074-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b074-106">Parameters</span></span>

<span data-ttu-id="2b074-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2b074-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b074-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b074-108">Return value</span></span>

<span data-ttu-id="2b074-109">Непредвиденное значение: S \_ (ОК или E) \_ .</span><span class="sxs-lookup"><span data-stu-id="2b074-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b074-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b074-110">Remarks</span></span>

<span data-ttu-id="2b074-111">Метод [**ксаурцестреам:: Inactive**](csourcestream-inactive.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="2b074-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b074-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2b074-112">Requirements</span></span>



| <span data-ttu-id="2b074-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2b074-113">Requirement</span></span> | <span data-ttu-id="2b074-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2b074-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b074-115">Header</span><span class="sxs-lookup"><span data-stu-id="2b074-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2b074-116"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b074-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2b074-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b074-117">Library</span></span><br/> | <dl> <span data-ttu-id="2b074-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2b074-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b074-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b074-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b074-120">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="2b074-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




