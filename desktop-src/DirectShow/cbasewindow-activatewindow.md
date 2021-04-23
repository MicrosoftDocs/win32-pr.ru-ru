---
description: Метод Активатевиндов изменяет размер окна в соответствии с требованиями производного класса.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Кбасевиндов. Активатевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675966"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="805ee-103">Кбасевиндов. Активатевиндов, метод</span><span class="sxs-lookup"><span data-stu-id="805ee-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="805ee-104">`ActivateWindow`Метод изменяет размер окна в соответствии с требованиями производного класса.</span><span class="sxs-lookup"><span data-stu-id="805ee-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="805ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="805ee-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="805ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="805ee-106">Parameters</span></span>

<span data-ttu-id="805ee-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="805ee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="805ee-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="805ee-108">Return value</span></span>

<span data-ttu-id="805ee-109">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="805ee-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="805ee-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="805ee-110">Return code</span></span>                                                                             | <span data-ttu-id="805ee-111">Описание</span><span class="sxs-lookup"><span data-stu-id="805ee-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="805ee-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="805ee-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="805ee-113">Окно уже активировано.</span><span class="sxs-lookup"><span data-stu-id="805ee-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="805ee-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="805ee-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="805ee-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="805ee-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="805ee-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="805ee-116">Remarks</span></span>

<span data-ttu-id="805ee-117">Этот метод вызывает метод [**кбасевиндов:: жетдефаултрект**](cbasewindow-getdefaultrect.md) для определения размера окна.</span><span class="sxs-lookup"><span data-stu-id="805ee-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="805ee-118">Производный класс должен переопределять **жетдефаултрект** для получения размера отображаемых изображений.</span><span class="sxs-lookup"><span data-stu-id="805ee-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="805ee-119">Если окно уже активно, вызов `ActivateWindow` перемещает окно в начало Z-порядка, но не изменяет размер окна.</span><span class="sxs-lookup"><span data-stu-id="805ee-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="805ee-120">То же самое верно, если у окна есть родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="805ee-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="805ee-121">Требования</span><span class="sxs-lookup"><span data-stu-id="805ee-121">Requirements</span></span>



| <span data-ttu-id="805ee-122">Требование</span><span class="sxs-lookup"><span data-stu-id="805ee-122">Requirement</span></span> | <span data-ttu-id="805ee-123">Значение</span><span class="sxs-lookup"><span data-stu-id="805ee-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805ee-124">Header</span><span class="sxs-lookup"><span data-stu-id="805ee-124">Header</span></span><br/>  | <dl> <span data-ttu-id="805ee-125"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="805ee-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="805ee-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="805ee-126">Library</span></span><br/> | <dl> <span data-ttu-id="805ee-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="805ee-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805ee-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="805ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805ee-129">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="805ee-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




