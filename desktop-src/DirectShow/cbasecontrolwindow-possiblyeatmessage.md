---
description: Метод Поссиблеатмессаже направляет сообщения клавиатуры и мыши в окно сток сообщений.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Кбасеконтролвиндов. Поссиблеатмессаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657190"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="3b53d-103">Кбасеконтролвиндов. Поссиблеатмессаже, метод</span><span class="sxs-lookup"><span data-stu-id="3b53d-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="3b53d-104">`PossiblyEatMessage`Метод пересылает сообщения клавиатуры и мыши в окно сток сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b53d-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b53d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b53d-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="3b53d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b53d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b53d-107">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="3b53d-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="3b53d-108">Окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b53d-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="3b53d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b53d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b53d-110">Первый параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b53d-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3b53d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b53d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b53d-112">Второй параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b53d-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b53d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b53d-113">Return value</span></span>

<span data-ttu-id="3b53d-114">Возвращает **значение true** , если сообщение было перенаправлено в окно, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3b53d-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b53d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b53d-115">Remarks</span></span>

<span data-ttu-id="3b53d-116">Окно сток сообщений — это окно, предназначенное для получения определенных сообщений мыши и клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="3b53d-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="3b53d-117">Изначально окно имеет **значение NULL**; его можно задать, вызвав [**кбасеконтролвиндов::p UT \_ мессажедраин**](cbasecontrolwindow-put-messagedrain.md).</span><span class="sxs-lookup"><span data-stu-id="3b53d-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="3b53d-118">Если окно стока сообщений не имеет **значение NULL**, `PossiblyEatMessage` в окно отправляется следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="3b53d-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="3b53d-119">WM \_ char</span><span class="sxs-lookup"><span data-stu-id="3b53d-119">WM\_CHAR</span></span>
-   <span data-ttu-id="3b53d-120">WM \_ деадчар</span><span class="sxs-lookup"><span data-stu-id="3b53d-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="3b53d-121">WM \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="3b53d-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="3b53d-122">WM \_ KEYUP</span><span class="sxs-lookup"><span data-stu-id="3b53d-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="3b53d-123">WM \_ лбуттондблклк</span><span class="sxs-lookup"><span data-stu-id="3b53d-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3b53d-124">WM \_ лбуттондовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="3b53d-125">WM \_ лбуттонуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="3b53d-126">WM \_ мбуттондблклк</span><span class="sxs-lookup"><span data-stu-id="3b53d-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3b53d-127">WM \_ мбуттондовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="3b53d-128">WM \_ мбуттонуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="3b53d-129">WM \_ маусеактивате</span><span class="sxs-lookup"><span data-stu-id="3b53d-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="3b53d-130">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="3b53d-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="3b53d-131">WM \_ нклбуттондблклк</span><span class="sxs-lookup"><span data-stu-id="3b53d-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3b53d-132">WM \_ нклбуттондовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="3b53d-133">WM \_ нклбуттонуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="3b53d-134">WM \_ нкмбуттондблклк</span><span class="sxs-lookup"><span data-stu-id="3b53d-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3b53d-135">WM \_ нкмбуттондовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="3b53d-136">WM \_ нкмбуттонуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="3b53d-137">WM \_ нкмаусемове</span><span class="sxs-lookup"><span data-stu-id="3b53d-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="3b53d-138">WM \_ нкрбуттондблклк</span><span class="sxs-lookup"><span data-stu-id="3b53d-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3b53d-139">WM \_ нкрбуттондовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="3b53d-140">WM \_ нкрбуттонуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="3b53d-141">WM \_ рбуттондблклк</span><span class="sxs-lookup"><span data-stu-id="3b53d-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3b53d-142">WM \_ рбуттондовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="3b53d-143">WM \_ рбуттонуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="3b53d-144">WM \_ сисчар</span><span class="sxs-lookup"><span data-stu-id="3b53d-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="3b53d-145">WM \_ сисдеадчар</span><span class="sxs-lookup"><span data-stu-id="3b53d-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="3b53d-146">WM \_ сискэйдовн</span><span class="sxs-lookup"><span data-stu-id="3b53d-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="3b53d-147">WM \_ сискэйуп</span><span class="sxs-lookup"><span data-stu-id="3b53d-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="3b53d-148">Другие сообщения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3b53d-148">It ignores other messages.</span></span> <span data-ttu-id="3b53d-149">Если окно сток сообщений имеет **значение NULL**, метод игнорирует все сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="3b53d-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="3b53d-150">Метод возвращает **значение true** , если отправляет сообщение, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3b53d-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="3b53d-151">Класс **кбасевиндов** вызывает этот метод при получении сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="3b53d-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b53d-152">Требования</span><span class="sxs-lookup"><span data-stu-id="3b53d-152">Requirements</span></span>



| <span data-ttu-id="3b53d-153">Требование</span><span class="sxs-lookup"><span data-stu-id="3b53d-153">Requirement</span></span> | <span data-ttu-id="3b53d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3b53d-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b53d-155">Header</span><span class="sxs-lookup"><span data-stu-id="3b53d-155">Header</span></span><br/>  | <dl> <span data-ttu-id="3b53d-156"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b53d-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b53d-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b53d-157">Library</span></span><br/> | <dl> <span data-ttu-id="3b53d-158"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3b53d-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b53d-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b53d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b53d-160">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="3b53d-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




