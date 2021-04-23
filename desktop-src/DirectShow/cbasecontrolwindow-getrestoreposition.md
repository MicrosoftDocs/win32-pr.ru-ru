---
description: Метод Жетресторепоситион извлекает расположение, в которое окно будет восстановлено, если оно не развернуто или не развернуто.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Кбасеконтролвиндов. Жетресторепоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657317"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="53f9b-103">Кбасеконтролвиндов. Жетресторепоситион, метод</span><span class="sxs-lookup"><span data-stu-id="53f9b-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="53f9b-104">`GetRestorePosition`Метод получает расположение, в которое будет восстановлено окно, если оно не развернуто или не развернуто.</span><span class="sxs-lookup"><span data-stu-id="53f9b-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f9b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53f9b-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="53f9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53f9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f9b-107">*плефт*</span><span class="sxs-lookup"><span data-stu-id="53f9b-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="53f9b-108">Указатель на значение для самой левой координаты.</span><span class="sxs-lookup"><span data-stu-id="53f9b-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="53f9b-109">*птоп*</span><span class="sxs-lookup"><span data-stu-id="53f9b-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="53f9b-110">Указатель на значение в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="53f9b-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="53f9b-111">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="53f9b-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="53f9b-112">Указатель на значение ширины окна.</span><span class="sxs-lookup"><span data-stu-id="53f9b-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="53f9b-113">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="53f9b-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="53f9b-114">Указатель на значение высоты окна.</span><span class="sxs-lookup"><span data-stu-id="53f9b-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f9b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53f9b-115">Return value</span></span>

<span data-ttu-id="53f9b-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53f9b-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f9b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53f9b-117">Remarks</span></span>

<span data-ttu-id="53f9b-118">Это то же самое, что и значения, возвращаемые функцией [**кбасеконтролвиндов:: жетвиндовпоситион**](cbasecontrolwindow-getwindowposition.md) , если окно не развернуто или не уменьшено.</span><span class="sxs-lookup"><span data-stu-id="53f9b-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f9b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="53f9b-119">Requirements</span></span>



| <span data-ttu-id="53f9b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="53f9b-120">Requirement</span></span> | <span data-ttu-id="53f9b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="53f9b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f9b-122">Header</span><span class="sxs-lookup"><span data-stu-id="53f9b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="53f9b-123"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53f9b-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="53f9b-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53f9b-124">Library</span></span><br/> | <dl> <span data-ttu-id="53f9b-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="53f9b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f9b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53f9b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f9b-127">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="53f9b-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




