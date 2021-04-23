---
description: Метод вставить \_ заголовок задает заголовок окна или заголовок.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Метод CBaseControlWindow.put_Caption (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657349"
---
# <a name="cbasecontrolwindowput_caption-method"></a><span data-ttu-id="f8b44-103">Метод Кбасеконтролвиндов. размещение \_ субтитров</span><span class="sxs-lookup"><span data-stu-id="f8b44-103">CBaseControlWindow.put\_Caption method</span></span>

<span data-ttu-id="f8b44-104">`put_Caption`Метод задает заголовок окна или заголовок.</span><span class="sxs-lookup"><span data-stu-id="f8b44-104">The `put_Caption` method sets the window title or caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8b44-105">Syntax</span></span>


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a><span data-ttu-id="f8b44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b44-107">*стркаптион*</span><span class="sxs-lookup"><span data-stu-id="f8b44-107">*strCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="f8b44-108">Новый заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="f8b44-108">New window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b44-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8b44-109">Return value</span></span>

<span data-ttu-id="f8b44-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8b44-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b44-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8b44-111">Remarks</span></span>

<span data-ttu-id="f8b44-112">Большинство окон верхнего уровня на рабочем столе под управлением Windows имеют заголовок (заголовок), связанный с ними.</span><span class="sxs-lookup"><span data-stu-id="f8b44-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="f8b44-113">Это свойство можно запрашивать и задавать с помощью интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="f8b44-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="f8b44-114">Любой набор заголовков будет виден только в том случае, если для окна \_ применен стиль «заголовок WS».</span><span class="sxs-lookup"><span data-stu-id="f8b44-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="f8b44-115">Если это не так, заголовок можно по-прежнему задать (и получить), хотя он не будет виден пользователю.</span><span class="sxs-lookup"><span data-stu-id="f8b44-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b44-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f8b44-116">Requirements</span></span>



| <span data-ttu-id="f8b44-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f8b44-117">Requirement</span></span> | <span data-ttu-id="f8b44-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f8b44-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b44-119">Header</span><span class="sxs-lookup"><span data-stu-id="f8b44-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f8b44-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b44-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8b44-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8b44-121">Library</span></span><br/> | <dl> <span data-ttu-id="f8b44-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b44-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b44-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8b44-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b44-124">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="f8b44-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




