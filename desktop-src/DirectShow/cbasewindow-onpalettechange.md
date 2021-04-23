---
description: Метод Онпалеттечанже обрабатывает сообщения изменения палитры.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Кбасевиндов. Онпалеттечанже, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675088"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="d02b2-103">Кбасевиндов. Онпалеттечанже, метод</span><span class="sxs-lookup"><span data-stu-id="d02b2-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="d02b2-104">`OnPaletteChange`Метод обрабатывает сообщения изменения палитры.</span><span class="sxs-lookup"><span data-stu-id="d02b2-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d02b2-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="d02b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d02b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02b2-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d02b2-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d02b2-108">Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="d02b2-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="d02b2-109">*Message*</span><span class="sxs-lookup"><span data-stu-id="d02b2-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="d02b2-110">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="d02b2-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02b2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d02b2-111">Return value</span></span>

<span data-ttu-id="d02b2-112">Возвращает 0, если сообщение было обработано, или значение 1, если сообщение не было обработано.</span><span class="sxs-lookup"><span data-stu-id="d02b2-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d02b2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d02b2-113">Remarks</span></span>

<span data-ttu-id="d02b2-114">Этот метод обрабатывает \_ сообщения WM палеттечанжед и WM \_ куериневпалетте.</span><span class="sxs-lookup"><span data-stu-id="d02b2-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="d02b2-115">Он вызывает метод [**кбасевиндов::D ореалисепалетте**](cbasewindow-dorealisepalette.md) для реализации новой палитры.</span><span class="sxs-lookup"><span data-stu-id="d02b2-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="d02b2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d02b2-116">Requirements</span></span>



| <span data-ttu-id="d02b2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d02b2-117">Requirement</span></span> | <span data-ttu-id="d02b2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d02b2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d02b2-119">Header</span><span class="sxs-lookup"><span data-stu-id="d02b2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d02b2-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d02b2-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d02b2-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d02b2-121">Library</span></span><br/> | <dl> <span data-ttu-id="d02b2-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d02b2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02b2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d02b2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02b2-124">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="d02b2-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




