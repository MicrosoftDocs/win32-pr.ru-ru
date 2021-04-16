---
description: Метод Сетвиндовпоситион задает расположение окна на рабочем столе.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Кбасеконтролвиндов. Сетвиндовпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657598"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="16a32-103">Кбасеконтролвиндов. Сетвиндовпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="16a32-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="16a32-104">`SetWindowPosition`Метод задает расположение окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="16a32-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16a32-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="16a32-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16a32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a32-107">*Слева*</span><span class="sxs-lookup"><span data-stu-id="16a32-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="16a32-108">Новая левая координата.</span><span class="sxs-lookup"><span data-stu-id="16a32-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="16a32-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="16a32-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="16a32-110">Новая Верхняя координата.</span><span class="sxs-lookup"><span data-stu-id="16a32-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="16a32-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="16a32-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="16a32-112">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="16a32-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="16a32-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="16a32-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="16a32-114">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="16a32-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a32-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16a32-115">Return value</span></span>

<span data-ttu-id="16a32-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16a32-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a32-117">Требования</span><span class="sxs-lookup"><span data-stu-id="16a32-117">Requirements</span></span>



| <span data-ttu-id="16a32-118">Требование</span><span class="sxs-lookup"><span data-stu-id="16a32-118">Requirement</span></span> | <span data-ttu-id="16a32-119">Значение</span><span class="sxs-lookup"><span data-stu-id="16a32-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a32-120">Header</span><span class="sxs-lookup"><span data-stu-id="16a32-120">Header</span></span><br/>  | <dl> <span data-ttu-id="16a32-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16a32-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="16a32-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16a32-122">Library</span></span><br/> | <dl> <span data-ttu-id="16a32-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="16a32-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a32-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16a32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a32-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="16a32-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




