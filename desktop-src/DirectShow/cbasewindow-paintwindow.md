---
description: Метод Паинтвиндов вызывает перерисовку окна.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Кбасевиндов. Паинтвиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657955"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="94fcd-103">Кбасевиндов. Паинтвиндов, метод</span><span class="sxs-lookup"><span data-stu-id="94fcd-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="94fcd-104">`PaintWindow`Метод вызывает перерисовку окна.</span><span class="sxs-lookup"><span data-stu-id="94fcd-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="94fcd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94fcd-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="94fcd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94fcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94fcd-107">*берасе*</span><span class="sxs-lookup"><span data-stu-id="94fcd-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="94fcd-108">Логическое значение, указывающее, удаляется ли фон.</span><span class="sxs-lookup"><span data-stu-id="94fcd-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="94fcd-109">Если значение равно **true**, фон удаляется.</span><span class="sxs-lookup"><span data-stu-id="94fcd-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94fcd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94fcd-110">Return value</span></span>

<span data-ttu-id="94fcd-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="94fcd-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94fcd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94fcd-112">Remarks</span></span>

<span data-ttu-id="94fcd-113">Этот метод создает сообщение WM \_ Paint путем непроверки всей клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="94fcd-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="94fcd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="94fcd-114">Requirements</span></span>



| <span data-ttu-id="94fcd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="94fcd-115">Requirement</span></span> | <span data-ttu-id="94fcd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="94fcd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fcd-117">Header</span><span class="sxs-lookup"><span data-stu-id="94fcd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="94fcd-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94fcd-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94fcd-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94fcd-119">Library</span></span><br/> | <dl> <span data-ttu-id="94fcd-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="94fcd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94fcd-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94fcd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fcd-122">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="94fcd-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




