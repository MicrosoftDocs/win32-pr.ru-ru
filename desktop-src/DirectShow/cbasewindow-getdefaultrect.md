---
description: Метод Жетдефаултрект Извлекает размер клиентской области по умолчанию.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Кбасевиндов. Жетдефаултрект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675474"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="5d21b-103">Кбасевиндов. Жетдефаултрект, метод</span><span class="sxs-lookup"><span data-stu-id="5d21b-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="5d21b-104">`GetDefaultRect`Метод получает размер клиентской области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d21b-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d21b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d21b-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="5d21b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d21b-106">Parameters</span></span>

<span data-ttu-id="5d21b-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5d21b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d21b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d21b-108">Return value</span></span>

<span data-ttu-id="5d21b-109">Возвращает прямоугольник по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d21b-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d21b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d21b-110">Remarks</span></span>

<span data-ttu-id="5d21b-111">Когда окно активируется, объект вызывает этот метод, чтобы определить, насколько крупнее он должен сделать клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="5d21b-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="5d21b-112">В базовом классе этот метод возвращает прямоугольник, высота и ширина которого являются определенными константами ДЕФХЕИГХТ и ДЕФВИДС.</span><span class="sxs-lookup"><span data-stu-id="5d21b-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="5d21b-113">Производный класс должен переопределять этот метод.</span><span class="sxs-lookup"><span data-stu-id="5d21b-113">A derived class should override this method.</span></span> <span data-ttu-id="5d21b-114">Для модуля обработки видео производный класс обычно возвращает размер собственного видеообраза.</span><span class="sxs-lookup"><span data-stu-id="5d21b-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d21b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5d21b-115">Requirements</span></span>



| <span data-ttu-id="5d21b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5d21b-116">Requirement</span></span> | <span data-ttu-id="5d21b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5d21b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d21b-118">Header</span><span class="sxs-lookup"><span data-stu-id="5d21b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5d21b-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d21b-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d21b-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d21b-120">Library</span></span><br/> | <dl> <span data-ttu-id="5d21b-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5d21b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d21b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d21b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d21b-123">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="5d21b-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




