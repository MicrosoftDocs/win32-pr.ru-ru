---
description: Посылается окну, когда его неклиентская область необходимо изменить, чтобы указать активное или неактивное состояние.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Сообщение WM_NCACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673823"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="1793e-103">\_Сообщение НКАКТИВАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="1793e-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="1793e-104">Посылается окну, когда его неклиентская область необходимо изменить, чтобы указать активное или неактивное состояние.</span><span class="sxs-lookup"><span data-stu-id="1793e-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="1793e-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1793e-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="1793e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1793e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1793e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1793e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1793e-108">Указывает, что необходимо изменить строку заголовка или значок, чтобы они указывали на активное или неактивное состояние.</span><span class="sxs-lookup"><span data-stu-id="1793e-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="1793e-109">При прорисовке активной строки заголовка или значка параметр *wParam* имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1793e-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="1793e-110">При прорисовке неактивной строки заголовка или значка *wParam* имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1793e-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1793e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1793e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1793e-112">Если для этого окна активен [визуальный стиль](../controls/themes-overview.md) , этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1793e-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="1793e-113">Если для этого окна неактивен визуальный стиль, этот параметр является маркером необязательного региона обновления для неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="1793e-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="1793e-114">Если этот параметр имеет значение-1, [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) не перерисовывает неклиентскую область, чтобы отразить изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="1793e-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1793e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1793e-115">Return value</span></span>

<span data-ttu-id="1793e-116">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="1793e-116">Type: **LRESULT**</span></span>

<span data-ttu-id="1793e-117">Если параметр *wParam* имеет **значение false**, приложение должно возвращать **значение true** , чтобы указать, что система должна продолжить обработку по умолчанию, или вернуть **значение false** , чтобы предотвратить изменение.</span><span class="sxs-lookup"><span data-stu-id="1793e-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="1793e-118">Если параметр *wParam* имеет **значение true**, возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1793e-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1793e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1793e-119">Remarks</span></span>

<span data-ttu-id="1793e-120">Не рекомендуется обрабатывать сообщения, связанные с неклиентской областью стандартного окна, так как приложение должно иметь возможность рисовать все необходимые части неклиентской области для окна.</span><span class="sxs-lookup"><span data-stu-id="1793e-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="1793e-121">Если приложение обрабатывает это сообщение, оно должно вернуть **значение true** , чтобы система занаправляла изменение активного окна.</span><span class="sxs-lookup"><span data-stu-id="1793e-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="1793e-122">Если окно свернется при получении сообщения, приложение должно передать сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="1793e-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="1793e-123">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) рисует строку заголовка или заголовок значка в его активных цветах, когда параметр *wParam* имеет **значение true** , а неактивные цвета *— в случае* **false**.</span><span class="sxs-lookup"><span data-stu-id="1793e-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1793e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1793e-124">Requirements</span></span>



| <span data-ttu-id="1793e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1793e-125">Requirement</span></span> | <span data-ttu-id="1793e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1793e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1793e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1793e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1793e-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1793e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1793e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1793e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1793e-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1793e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1793e-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1793e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1793e-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1793e-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1793e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1793e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="1793e-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1793e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1793e-135">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="1793e-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="1793e-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1793e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1793e-137">Windows</span><span class="sxs-lookup"><span data-stu-id="1793e-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
