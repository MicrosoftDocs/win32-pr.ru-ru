---
description: Метод Жетвиндовпоситион извлекает текущие координаты окна.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Кбасеконтролвиндов. Жетвиндовпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657316"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="9071e-103">Кбасеконтролвиндов. Жетвиндовпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="9071e-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="9071e-104">`GetWindowPosition`Метод получает текущие координаты окна.</span><span class="sxs-lookup"><span data-stu-id="9071e-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9071e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9071e-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="9071e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9071e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9071e-107">*плефт*</span><span class="sxs-lookup"><span data-stu-id="9071e-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="9071e-108">Указатель на левую координату в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="9071e-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9071e-109">*птоп*</span><span class="sxs-lookup"><span data-stu-id="9071e-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="9071e-110">Указатель на верхнюю координату в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="9071e-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9071e-111">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="9071e-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="9071e-112">Указатель на ширину окна в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="9071e-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9071e-113">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="9071e-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="9071e-114">Указатель на высоту окна в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="9071e-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9071e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9071e-115">Return value</span></span>

<span data-ttu-id="9071e-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9071e-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9071e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9071e-117">Requirements</span></span>



| <span data-ttu-id="9071e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9071e-118">Requirement</span></span> | <span data-ttu-id="9071e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9071e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9071e-120">Header</span><span class="sxs-lookup"><span data-stu-id="9071e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9071e-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9071e-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9071e-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9071e-122">Library</span></span><br/> | <dl> <span data-ttu-id="9071e-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9071e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9071e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9071e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9071e-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="9071e-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




