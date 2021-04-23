---
description: Метод Сетдравконтекст задает контексты устройств, используемые для рисования.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Кдравимаже. Сетдравконтекст, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657146"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="1f8fa-103">Кдравимаже. Сетдравконтекст, метод</span><span class="sxs-lookup"><span data-stu-id="1f8fa-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="1f8fa-104">`SetDrawContext`Метод задает контексты устройств, используемые для рисования.</span><span class="sxs-lookup"><span data-stu-id="1f8fa-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f8fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f8fa-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="1f8fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f8fa-106">Parameters</span></span>

<span data-ttu-id="1f8fa-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1f8fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f8fa-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f8fa-108">Return value</span></span>

<span data-ttu-id="1f8fa-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1f8fa-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f8fa-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f8fa-110">Remarks</span></span>

<span data-ttu-id="1f8fa-111">Этот метод получает контексты окна и устройства памяти из объекта-владельца [**кбасевиндов**](cbasewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8fa-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="1f8fa-112">Вызывайте этот метод после инициализации окна, но перед началом рисования.</span><span class="sxs-lookup"><span data-stu-id="1f8fa-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f8fa-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1f8fa-113">Requirements</span></span>



| <span data-ttu-id="1f8fa-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1f8fa-114">Requirement</span></span> | <span data-ttu-id="1f8fa-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1f8fa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8fa-116">Header</span><span class="sxs-lookup"><span data-stu-id="1f8fa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1f8fa-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f8fa-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f8fa-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f8fa-118">Library</span></span><br/> | <dl> <span data-ttu-id="1f8fa-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1f8fa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f8fa-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f8fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f8fa-121">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="1f8fa-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




