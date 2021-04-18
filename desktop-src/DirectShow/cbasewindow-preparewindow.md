---
description: Метод Препаревиндов создает окно.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Кбасевиндов. Препаревиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657954"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="43870-103">Кбасевиндов. Препаревиндов, метод</span><span class="sxs-lookup"><span data-stu-id="43870-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="43870-104">`PrepareWindow`Метод создает окно.</span><span class="sxs-lookup"><span data-stu-id="43870-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="43870-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43870-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="43870-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43870-106">Parameters</span></span>

<span data-ttu-id="43870-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="43870-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43870-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43870-108">Return value</span></span>

<span data-ttu-id="43870-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43870-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="43870-110">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="43870-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="43870-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43870-111">Return code</span></span>                                                                            | <span data-ttu-id="43870-112">Описание</span><span class="sxs-lookup"><span data-stu-id="43870-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="43870-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="43870-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="43870-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="43870-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="43870-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="43870-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="43870-116">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="43870-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43870-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43870-117">Remarks</span></span>

<span data-ttu-id="43870-118">Вызовите этот метод после создания объекта.</span><span class="sxs-lookup"><span data-stu-id="43870-118">Call this method after creating the object.</span></span> <span data-ttu-id="43870-119">Этот метод выполняет некоторый первоначальный бухгалтерский вызов, а затем вызывает метод [**кбасевиндов::D окреатевиндов**](cbasewindow-docreatewindow.md) для создания окна.</span><span class="sxs-lookup"><span data-stu-id="43870-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="43870-120">Требования</span><span class="sxs-lookup"><span data-stu-id="43870-120">Requirements</span></span>



| <span data-ttu-id="43870-121">Требование</span><span class="sxs-lookup"><span data-stu-id="43870-121">Requirement</span></span> | <span data-ttu-id="43870-122">Значение</span><span class="sxs-lookup"><span data-stu-id="43870-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43870-123">Header</span><span class="sxs-lookup"><span data-stu-id="43870-123">Header</span></span><br/>  | <dl> <span data-ttu-id="43870-124"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43870-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43870-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43870-125">Library</span></span><br/> | <dl> <span data-ttu-id="43870-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="43870-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43870-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43870-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43870-128">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="43870-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




