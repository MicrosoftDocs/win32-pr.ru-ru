---
description: Посылается, когда приложение изменяет включенное состояние окна.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Сообщение WM_ENABLE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693280"
---
# <a name="wm_enable-message"></a><span data-ttu-id="9f584-103">\_Сообщение о включении WM</span><span class="sxs-lookup"><span data-stu-id="9f584-103">WM\_ENABLE message</span></span>

<span data-ttu-id="9f584-104">Посылается, когда приложение изменяет включенное состояние окна.</span><span class="sxs-lookup"><span data-stu-id="9f584-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="9f584-105">Он отправляется в окно, состояние которого разрешено изменить.</span><span class="sxs-lookup"><span data-stu-id="9f584-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="9f584-106">Это сообщение отправляется перед возвратом функции [**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow) , но после изменения включенного состояния (бит [**\_ отключенного типа WS**](window-styles.md) ) окна.</span><span class="sxs-lookup"><span data-stu-id="9f584-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="9f584-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9f584-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="9f584-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f584-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f584-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f584-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f584-110">Указывает, было ли окно включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="9f584-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="9f584-111">Этот параметр имеет **значение true** , если окно было включено, или **значение false** , если окно было отключено.</span><span class="sxs-lookup"><span data-stu-id="9f584-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="9f584-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f584-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f584-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="9f584-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f584-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f584-114">Return value</span></span>

<span data-ttu-id="9f584-115">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="9f584-115">Type: **LRESULT**</span></span>

<span data-ttu-id="9f584-116">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="9f584-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f584-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9f584-117">Requirements</span></span>



| <span data-ttu-id="9f584-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9f584-118">Requirement</span></span> | <span data-ttu-id="9f584-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9f584-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f584-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f584-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9f584-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f584-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9f584-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f584-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9f584-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f584-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f584-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f584-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f584-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f584-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f584-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f584-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f584-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9f584-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f584-128">**енаблевиндов**</span><span class="sxs-lookup"><span data-stu-id="9f584-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="9f584-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9f584-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f584-130">Windows</span><span class="sxs-lookup"><span data-stu-id="9f584-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
