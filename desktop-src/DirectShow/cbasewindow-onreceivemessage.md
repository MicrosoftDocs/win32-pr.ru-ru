---
description: Метод Онрецеивемессаже обрабатывает сообщения окна.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Кбасевиндов. Онрецеивемессаже, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657037"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="7cea0-103">Кбасевиндов. Онрецеивемессаже, метод</span><span class="sxs-lookup"><span data-stu-id="7cea0-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="7cea0-104">`OnReceiveMessage`Метод обрабатывает сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="7cea0-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cea0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cea0-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="7cea0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cea0-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="7cea0-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7cea0-108">Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="7cea0-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="7cea0-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="7cea0-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="7cea0-110">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="7cea0-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7cea0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7cea0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cea0-112">Первый параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="7cea0-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7cea0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7cea0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cea0-114">Второй параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="7cea0-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cea0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cea0-115">Return value</span></span>

<span data-ttu-id="7cea0-116">Возвращает 0, если сообщение было обработано, или значение 1, если сообщение не было обработано.</span><span class="sxs-lookup"><span data-stu-id="7cea0-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cea0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cea0-117">Remarks</span></span>

<span data-ttu-id="7cea0-118">Базовый класс обрабатывает следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="7cea0-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="7cea0-119">\_Закрыть WM</span><span class="sxs-lookup"><span data-stu-id="7cea0-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="7cea0-120">\_Перемещение WM</span><span class="sxs-lookup"><span data-stu-id="7cea0-120">WM\_MOVE</span></span>
-   <span data-ttu-id="7cea0-121">WM \_ палеттечанжед</span><span class="sxs-lookup"><span data-stu-id="7cea0-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="7cea0-122">WM \_ куериневпалетте</span><span class="sxs-lookup"><span data-stu-id="7cea0-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="7cea0-123">\_Размер WM</span><span class="sxs-lookup"><span data-stu-id="7cea0-123">WM\_SIZE</span></span>
-   <span data-ttu-id="7cea0-124">WM \_ сисколорчанже</span><span class="sxs-lookup"><span data-stu-id="7cea0-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="7cea0-125">Производный класс может переопределить этот метод для управления другими сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7cea0-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="7cea0-126">Производный класс должен вызвать метод базового класса, чтобы обрабатывать все сообщения, которые пропускаются производным классом.</span><span class="sxs-lookup"><span data-stu-id="7cea0-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cea0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7cea0-127">Requirements</span></span>



| <span data-ttu-id="7cea0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7cea0-128">Requirement</span></span> | <span data-ttu-id="7cea0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7cea0-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cea0-130">Header</span><span class="sxs-lookup"><span data-stu-id="7cea0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7cea0-131"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cea0-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7cea0-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7cea0-132">Library</span></span><br/> | <dl> <span data-ttu-id="7cea0-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7cea0-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cea0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cea0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cea0-135">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="7cea0-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




