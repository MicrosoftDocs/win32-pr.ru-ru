---
description: Отправляется в окно, для которого пользователь изменяет размер. Обрабатывая это сообщение, приложение может отслеживать размер и расположение прямоугольника перетаскивания и, при необходимости, изменять его размер или расположение.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Сообщение WM_SIZING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813865"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="313dd-104">\_Сообщение о размере WM</span><span class="sxs-lookup"><span data-stu-id="313dd-104">WM\_SIZING message</span></span>

<span data-ttu-id="313dd-105">Отправляется в окно, для которого пользователь изменяет размер.</span><span class="sxs-lookup"><span data-stu-id="313dd-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="313dd-106">Обрабатывая это сообщение, приложение может отслеживать размер и расположение прямоугольника перетаскивания и, при необходимости, изменять его размер или расположение.</span><span class="sxs-lookup"><span data-stu-id="313dd-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="313dd-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="313dd-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="313dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="313dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="313dd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313dd-110">Граница окна, размер которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="313dd-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="313dd-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="313dd-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="313dd-112">Значение</span><span class="sxs-lookup"><span data-stu-id="313dd-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="313dd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="313dd-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="313dd-114"><dt>**Вмсз \_ Нижняя**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="313dd-115">Нижний край</span><span class="sxs-lookup"><span data-stu-id="313dd-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="313dd-116"><dt>**Вмсз \_ БОТТОМЛЕФТ**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="313dd-117">Левый нижний угол</span><span class="sxs-lookup"><span data-stu-id="313dd-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="313dd-118"><dt>**Вмсз \_ БОТТОМРИГХТ**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="313dd-119">Правый нижний угол</span><span class="sxs-lookup"><span data-stu-id="313dd-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="313dd-120"><dt>**Вмсз \_ СЛЕВА**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="313dd-121">Левый край</span><span class="sxs-lookup"><span data-stu-id="313dd-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="313dd-122"><dt>**Вмсз \_ СПРАВА**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="313dd-123">Правый край</span><span class="sxs-lookup"><span data-stu-id="313dd-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="313dd-124"><dt>**Вмсз \_ Первые**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="313dd-125">Верхний край</span><span class="sxs-lookup"><span data-stu-id="313dd-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="313dd-126"><dt>**Вмсз \_ ТОПЛЕФТ**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="313dd-127">Левый верхний угол</span><span class="sxs-lookup"><span data-stu-id="313dd-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="313dd-128"><dt>**Вмсз \_ ВЕРХНЕМ**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="313dd-129">Правый верхний угол</span><span class="sxs-lookup"><span data-stu-id="313dd-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="313dd-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="313dd-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313dd-131">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) с координатами экрана прямоугольника перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="313dd-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="313dd-132">Чтобы изменить размер или расположение прямоугольника перетаскивания, приложение должно изменить члены этой структуры.</span><span class="sxs-lookup"><span data-stu-id="313dd-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313dd-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="313dd-133">Return value</span></span>

<span data-ttu-id="313dd-134">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="313dd-134">Type: **LRESULT**</span></span>

<span data-ttu-id="313dd-135">Приложение должно возвращать **значение true** , если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="313dd-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="313dd-136">Требования</span><span class="sxs-lookup"><span data-stu-id="313dd-136">Requirements</span></span>



| <span data-ttu-id="313dd-137">Требование</span><span class="sxs-lookup"><span data-stu-id="313dd-137">Requirement</span></span> | <span data-ttu-id="313dd-138">Значение</span><span class="sxs-lookup"><span data-stu-id="313dd-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313dd-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="313dd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="313dd-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="313dd-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="313dd-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="313dd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="313dd-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="313dd-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="313dd-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="313dd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="313dd-144"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="313dd-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313dd-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="313dd-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="313dd-146">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="313dd-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="313dd-147">**\_Перемещение WM**</span><span class="sxs-lookup"><span data-stu-id="313dd-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="313dd-148">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="313dd-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="313dd-149">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="313dd-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="313dd-150">Windows</span><span class="sxs-lookup"><span data-stu-id="313dd-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="313dd-151">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="313dd-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="313dd-152">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="313dd-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
