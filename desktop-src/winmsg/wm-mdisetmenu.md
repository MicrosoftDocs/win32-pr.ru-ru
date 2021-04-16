---
description: Приложение отправляет \_ сообщение WM мдисетмену в окно клиента многодокументного интерфейса (MDI) для замены всего меню окна фрейма MDI, для замены меню окна фрейма окна или и того и другого.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Сообщение WM_MDISETMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719508"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="1e75d-103">\_Сообщение МДИСЕТМЕНУ WM</span><span class="sxs-lookup"><span data-stu-id="1e75d-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="1e75d-104">Приложение отправляет сообщение **WM \_ мдисетмену** в окно клиента многодокументного интерфейса (MDI) для замены всего меню окна фрейма MDI, для замены меню окна фрейма окна или и того и другого.</span><span class="sxs-lookup"><span data-stu-id="1e75d-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="1e75d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e75d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e75d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e75d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e75d-107">Маркер для нового меню окна фрейма.</span><span class="sxs-lookup"><span data-stu-id="1e75d-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="1e75d-108">Если этот параметр имеет **значение NULL**, меню окна фрейма не изменяется.</span><span class="sxs-lookup"><span data-stu-id="1e75d-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="1e75d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e75d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e75d-110">Маркер для нового меню "окно".</span><span class="sxs-lookup"><span data-stu-id="1e75d-110">A handle to the new window menu.</span></span> <span data-ttu-id="1e75d-111">Если этот параметр имеет **значение NULL**, меню окно не изменяется.</span><span class="sxs-lookup"><span data-stu-id="1e75d-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e75d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e75d-112">Return value</span></span>

<span data-ttu-id="1e75d-113">Тип: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="1e75d-113">Type: **HMENU**</span></span>

<span data-ttu-id="1e75d-114">Если сообщение прошло удачно, возвращаемое значение является маркером для старого меню окна фрейма.</span><span class="sxs-lookup"><span data-stu-id="1e75d-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="1e75d-115">Если сообщение не выполняется, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1e75d-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e75d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e75d-116">Remarks</span></span>

<span data-ttu-id="1e75d-117">После отправки этого сообщения приложение должно вызвать функцию [**дравменубар**](/windows/win32/api/winuser/nf-winuser-drawmenubar) для обновления строки меню.</span><span class="sxs-lookup"><span data-stu-id="1e75d-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="1e75d-118">Если это сообщение заменяет меню окна, пункты меню дочернего окна MDI удаляются из предыдущего меню окна и добавляются в меню новое окно.</span><span class="sxs-lookup"><span data-stu-id="1e75d-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="1e75d-119">Если дочернее окно MDI развернуто и это сообщение заменяет меню окна фрейма MDI, значок меню окна и значок восстановления удаляются из предыдущего меню окна фрейма и добавляются в новое меню окна фрейма.</span><span class="sxs-lookup"><span data-stu-id="1e75d-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e75d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1e75d-120">Requirements</span></span>



| <span data-ttu-id="1e75d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1e75d-121">Requirement</span></span> | <span data-ttu-id="1e75d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1e75d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e75d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e75d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e75d-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e75d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1e75d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e75d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e75d-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e75d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e75d-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e75d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e75d-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e75d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e75d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e75d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e75d-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1e75d-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e75d-131">**дравменубар**</span><span class="sxs-lookup"><span data-stu-id="1e75d-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="1e75d-132">**WM \_ мдирефрешмену**</span><span class="sxs-lookup"><span data-stu-id="1e75d-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="1e75d-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1e75d-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e75d-134">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="1e75d-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
