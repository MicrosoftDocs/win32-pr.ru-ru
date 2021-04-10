---
description: Отправляются в окно, размер, расположение или место в Z-порядке изменились в результате вызова функции SetWindowPos или другой функции управления окнами.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Сообщение WM_WINDOWPOSCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144713"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="a8b83-103">\_Сообщение ВИНДОВПОСЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="a8b83-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="a8b83-104">Отправляются в окно, размер, расположение или место в Z-порядке изменились в результате вызова функции [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) или другой функции управления окнами.</span><span class="sxs-lookup"><span data-stu-id="a8b83-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="a8b83-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a8b83-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="a8b83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8b83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b83-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8b83-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b83-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a8b83-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a8b83-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8b83-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b83-110">Указатель на структуру [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) , которая содержит сведения о новом размере и позиции окна.</span><span class="sxs-lookup"><span data-stu-id="a8b83-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b83-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8b83-111">Return value</span></span>

<span data-ttu-id="a8b83-112">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="a8b83-112">Type: **LRESULT**</span></span>

<span data-ttu-id="a8b83-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="a8b83-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b83-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8b83-114">Remarks</span></span>

<span data-ttu-id="a8b83-115">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет в окно [**сообщения \_ размером WM**](wm-size.md) и [**WM \_**](wm-move.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b83-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="a8b83-116">Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="a8b83-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="a8b83-117">Более эффективно выполнять любые операции перемещения или изменения размера во время сообщения **\_ виндовпосчанжед WM** без вызова **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="a8b83-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b83-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b83-118">Requirements</span></span>



| <span data-ttu-id="a8b83-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b83-119">Requirement</span></span> | <span data-ttu-id="a8b83-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b83-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b83-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8b83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b83-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a8b83-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8b83-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8b83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b83-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a8b83-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8b83-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a8b83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b83-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b83-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b83-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8b83-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8b83-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a8b83-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8b83-129">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="a8b83-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a8b83-130">**енддефервиндовпос**</span><span class="sxs-lookup"><span data-stu-id="a8b83-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="a8b83-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="a8b83-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="a8b83-132">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="a8b83-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="a8b83-133">**\_Перемещение WM**</span><span class="sxs-lookup"><span data-stu-id="a8b83-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="a8b83-134">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="a8b83-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="a8b83-135">**WM \_ виндовпосчангинг**</span><span class="sxs-lookup"><span data-stu-id="a8b83-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="a8b83-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a8b83-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a8b83-137">Windows</span><span class="sxs-lookup"><span data-stu-id="a8b83-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
