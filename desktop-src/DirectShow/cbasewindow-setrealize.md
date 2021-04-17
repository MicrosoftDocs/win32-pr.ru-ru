---
description: Метод Сетреализе указывает, реализует ли окно палитры.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Кбасевиндов. Сетреализе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679994"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="1ab78-103">Кбасевиндов. Сетреализе, метод</span><span class="sxs-lookup"><span data-stu-id="1ab78-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="1ab78-104">`SetRealize`Метод указывает, реализует ли окно палитры.</span><span class="sxs-lookup"><span data-stu-id="1ab78-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ab78-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="1ab78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ab78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab78-107">*бреализе*</span><span class="sxs-lookup"><span data-stu-id="1ab78-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab78-108">Логическое значение, указывающее, следует ли реализовывать палитры.</span><span class="sxs-lookup"><span data-stu-id="1ab78-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="1ab78-109">Если **значение равно true**, метод [**Кбасевиндов:: сетпалетте**](cbasewindow-setpalette.md) реализует палитры.</span><span class="sxs-lookup"><span data-stu-id="1ab78-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab78-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ab78-110">Return value</span></span>

<span data-ttu-id="1ab78-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1ab78-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ab78-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ab78-112">Remarks</span></span>

<span data-ttu-id="1ab78-113">По умолчанию метод **сетпалетте** реализует указанную палитру.</span><span class="sxs-lookup"><span data-stu-id="1ab78-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="1ab78-114">Вызовите этот метод, чтобы изменить поведение по умолчанию, чтобы палитры были выбраны, но не были реализованы.</span><span class="sxs-lookup"><span data-stu-id="1ab78-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="1ab78-115">Этот метод задает переменную члена [**кбасевиндов:: m \_ бнореализе**](cbasewindow-m-bnorealize.md) .</span><span class="sxs-lookup"><span data-stu-id="1ab78-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab78-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1ab78-116">Requirements</span></span>



| <span data-ttu-id="1ab78-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1ab78-117">Requirement</span></span> | <span data-ttu-id="1ab78-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1ab78-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab78-119">Header</span><span class="sxs-lookup"><span data-stu-id="1ab78-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1ab78-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ab78-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ab78-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ab78-121">Library</span></span><br/> | <dl> <span data-ttu-id="1ab78-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1ab78-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab78-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ab78-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab78-124">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="1ab78-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




