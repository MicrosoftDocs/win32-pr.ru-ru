---
description: Метод Жетовнервиндов Извлекает маркер окна-владельца m \_ хвндовнер.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Кбасеконтролвиндов. Жетовнервиндов, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657319"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="3c30f-103">Кбасеконтролвиндов. Жетовнервиндов, метод</span><span class="sxs-lookup"><span data-stu-id="3c30f-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="3c30f-104">`GetOwnerWindow`Метод получает маркер окна-владельца, **m \_ хвндовнер**.</span><span class="sxs-lookup"><span data-stu-id="3c30f-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c30f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c30f-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="3c30f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c30f-106">Parameters</span></span>

<span data-ttu-id="3c30f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3c30f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c30f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c30f-108">Return value</span></span>

<span data-ttu-id="3c30f-109">Возвращает окно владельца.</span><span class="sxs-lookup"><span data-stu-id="3c30f-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c30f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c30f-110">Remarks</span></span>

<span data-ttu-id="3c30f-111">Извлекает окно-владелец без вызова метода интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3c30f-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="3c30f-112">Используйте эту функцию-член вместо [**кбасеконтролвиндов:: Get \_ owner**](cbasecontrolwindow-get-owner.md), если только вы не вызываете ее извне с помощью метода [**ивидеовиндов:: Get \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .</span><span class="sxs-lookup"><span data-stu-id="3c30f-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c30f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3c30f-113">Requirements</span></span>



| <span data-ttu-id="3c30f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3c30f-114">Requirement</span></span> | <span data-ttu-id="3c30f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3c30f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-116">Header</span><span class="sxs-lookup"><span data-stu-id="3c30f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3c30f-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c30f-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c30f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c30f-118">Library</span></span><br/> | <dl> <span data-ttu-id="3c30f-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3c30f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c30f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c30f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c30f-121">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="3c30f-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




