---
description: Метод Сетвиндовфореграунд перемещает окно видео на передний план и при необходимости дает ему фокус.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Кбасеконтролвиндов. Сетвиндовфореграунд, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658058"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="663ac-103">Кбасеконтролвиндов. Сетвиндовфореграунд, метод</span><span class="sxs-lookup"><span data-stu-id="663ac-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="663ac-104">`SetWindowForeground`Метод перемещает окно видео на передний план и при необходимости дает ему фокус.</span><span class="sxs-lookup"><span data-stu-id="663ac-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="663ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="663ac-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="663ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="663ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="663ac-107">*Фокус*</span><span class="sxs-lookup"><span data-stu-id="663ac-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="663ac-108">Значение, указывающее, будет ли окно видео получать фокус.</span><span class="sxs-lookup"><span data-stu-id="663ac-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="663ac-109">Значение 1 задает фокус окна, а 0 — нет.</span><span class="sxs-lookup"><span data-stu-id="663ac-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="663ac-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="663ac-110">Return value</span></span>

<span data-ttu-id="663ac-111">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="663ac-111">Returns one of the following values.</span></span>



| <span data-ttu-id="663ac-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="663ac-112">Return code</span></span>                                                                                           | <span data-ttu-id="663ac-113">Описание</span><span class="sxs-lookup"><span data-stu-id="663ac-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="663ac-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="663ac-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="663ac-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="663ac-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="663ac-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="663ac-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="663ac-117">Фокус не равен 1 или 0.</span><span class="sxs-lookup"><span data-stu-id="663ac-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="663ac-118"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="663ac-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="663ac-119">Текущий фильтр не подключен к полному графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="663ac-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="663ac-120">Требования</span><span class="sxs-lookup"><span data-stu-id="663ac-120">Requirements</span></span>



| <span data-ttu-id="663ac-121">Требование</span><span class="sxs-lookup"><span data-stu-id="663ac-121">Requirement</span></span> | <span data-ttu-id="663ac-122">Значение</span><span class="sxs-lookup"><span data-stu-id="663ac-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="663ac-123">Header</span><span class="sxs-lookup"><span data-stu-id="663ac-123">Header</span></span><br/>  | <dl> <span data-ttu-id="663ac-124"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="663ac-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="663ac-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="663ac-125">Library</span></span><br/> | <dl> <span data-ttu-id="663ac-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="663ac-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="663ac-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="663ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="663ac-128">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="663ac-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




