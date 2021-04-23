---
description: Приложение отправляет \_ сообщение WM мдикреате в окно клиента многодокументного интерфейса (MDI) для создания дочернего окна MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Сообщение WM_MDICREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712349"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="35f22-103">\_Сообщение МДИКРЕАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="35f22-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="35f22-104">Приложение отправляет сообщение **WM \_ мдикреате** в окно клиента многодокументного интерфейса (MDI) для создания дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="35f22-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="35f22-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="35f22-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f22-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35f22-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35f22-107">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="35f22-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35f22-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35f22-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35f22-109">Указатель на структуру [**мдикреатеструкт**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) , содержащую сведения, которые система использует для создания дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="35f22-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f22-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35f22-110">Return value</span></span>

<span data-ttu-id="35f22-111">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="35f22-111">Type: **HWND**</span></span>

<span data-ttu-id="35f22-112">Если сообщение прошло удачно, возвращаемое значение является маркером нового дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="35f22-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="35f22-113">Если сообщение не выполняется, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="35f22-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="35f22-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35f22-114">Remarks</span></span>

<span data-ttu-id="35f22-115">Дочернее окно MDI создается с [**стилем окна**](window-styles.md) разрядов **WS \_ дочерний**, **WS \_ клипсиблингс**, **WS \_ клипчилдрен**, **WS \_** **\_ Минимизебокс** и **WS \_ максимизебокс** **, а \_** также дополнительными битами стиля, указанными в структуре [**мдикреатеструкт**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . **\_**</span><span class="sxs-lookup"><span data-stu-id="35f22-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="35f22-116">Система добавляет заголовок нового дочернего окна в меню окно фрейма окна.</span><span class="sxs-lookup"><span data-stu-id="35f22-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="35f22-117">Приложение должно использовать это сообщение для создания всех дочерних окон клиентского окна.</span><span class="sxs-lookup"><span data-stu-id="35f22-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="35f22-118">Если клиентское MDI-окно получает сообщение, которое изменяет активацию дочерних окон, когда активное дочернее окно развернуто, система восстанавливает активное дочернее окно и разворачивает вновь активированное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="35f22-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="35f22-119">При создании дочернего окна MDI система отправляет в окно сообщение [**о \_ создании WM**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="35f22-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="35f22-120">Параметр *lParam* сообщения **WM \_ CREATE** содержит указатель на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="35f22-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="35f22-121">Элемент *лпкреатепарамс* этой структуры содержит указатель на структуру [**мдикреатеструкт**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) , переданную с сообщением **WM \_ мдикреате** , которое создало дочернее окно MDI.</span><span class="sxs-lookup"><span data-stu-id="35f22-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="35f22-122">Приложение не должно отсылать второе сообщение **\_ мдикреате WM** , пока не будет обработано сообщение **\_ мдикреате WM** .</span><span class="sxs-lookup"><span data-stu-id="35f22-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="35f22-123">Например, он не должен отсылать сообщение **\_ мдикреате WM** , пока дочернее окно MDI обрабатывает сообщение **WM \_ мдикреате** .</span><span class="sxs-lookup"><span data-stu-id="35f22-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f22-124">Требования</span><span class="sxs-lookup"><span data-stu-id="35f22-124">Requirements</span></span>



| <span data-ttu-id="35f22-125">Требование</span><span class="sxs-lookup"><span data-stu-id="35f22-125">Requirement</span></span> | <span data-ttu-id="35f22-126">Значение</span><span class="sxs-lookup"><span data-stu-id="35f22-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35f22-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35f22-127">Minimum supported client</span></span><br/> | <span data-ttu-id="35f22-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35f22-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35f22-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35f22-129">Minimum supported server</span></span><br/> | <span data-ttu-id="35f22-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35f22-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35f22-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="35f22-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="35f22-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35f22-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f22-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35f22-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="35f22-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="35f22-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35f22-135">**креатемдивиндов**</span><span class="sxs-lookup"><span data-stu-id="35f22-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="35f22-136">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="35f22-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="35f22-137">**мдикреатеструкт**</span><span class="sxs-lookup"><span data-stu-id="35f22-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="35f22-138">**\_Создание WM**</span><span class="sxs-lookup"><span data-stu-id="35f22-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="35f22-139">**WM \_ мдидестрой**</span><span class="sxs-lookup"><span data-stu-id="35f22-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="35f22-140">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="35f22-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35f22-141">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="35f22-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
