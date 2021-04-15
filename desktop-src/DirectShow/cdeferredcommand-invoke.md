---
description: Метод Invoke предоставляет доступ к методам и свойствам, предоставляемым объектом.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Метод Кдеферредкомманд. Invoke (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675813"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="2cf78-103">Кдеферредкомманд. Invoke, метод</span><span class="sxs-lookup"><span data-stu-id="2cf78-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="2cf78-104">`Invoke`Метод предоставляет доступ к методам и свойствам, предоставляемым объектом.</span><span class="sxs-lookup"><span data-stu-id="2cf78-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cf78-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="2cf78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cf78-106">Parameters</span></span>

<span data-ttu-id="2cf78-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2cf78-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2cf78-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cf78-108">Return value</span></span>

<span data-ttu-id="2cf78-109">Возвращает VFW \_ E \_ уже \_ отменено, если **m \_ пкуеуе** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2cf78-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="2cf78-110">В противном случае возвращает **значение HRESULT** , полученное в результате вызова **IDispatch:: GetTypeInfo** или **IUnknown:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="2cf78-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf78-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2cf78-111">Requirements</span></span>



| <span data-ttu-id="2cf78-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2cf78-112">Requirement</span></span> | <span data-ttu-id="2cf78-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2cf78-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf78-114">Header</span><span class="sxs-lookup"><span data-stu-id="2cf78-114">Header</span></span><br/>  | <dl> <span data-ttu-id="2cf78-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf78-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2cf78-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2cf78-116">Library</span></span><br/> | <dl> <span data-ttu-id="2cf78-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf78-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf78-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cf78-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf78-119">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="2cf78-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




