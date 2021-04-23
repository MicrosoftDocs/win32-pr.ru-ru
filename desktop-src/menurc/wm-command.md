---
title: Сообщение WM_COMMAND (Winuser. h)
description: Посылается, когда пользователь выбирает элемент команды из меню, когда элемент управления отправляет сообщение уведомления родительскому окну или при преобразовании нажатия клавиши быстрого вызова.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708370"
---
# <a name="wm_command-message"></a><span data-ttu-id="b49e4-104">\_Командное сообщение WM</span><span class="sxs-lookup"><span data-stu-id="b49e4-104">WM\_COMMAND message</span></span>

<span data-ttu-id="b49e4-105">Посылается, когда пользователь выбирает элемент команды из меню, когда элемент управления отправляет сообщение уведомления родительскому окну или при преобразовании нажатия клавиши быстрого вызова.</span><span class="sxs-lookup"><span data-stu-id="b49e4-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="b49e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b49e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b49e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b49e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b49e4-108">Описание этого параметра см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="b49e4-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b49e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b49e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b49e4-110">Описание этого параметра см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="b49e4-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b49e4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b49e4-111">Return value</span></span>

<span data-ttu-id="b49e4-112">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="b49e4-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="b49e4-113">Пример</span><span class="sxs-lookup"><span data-stu-id="b49e4-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="b49e4-114">Пример, взятый из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="b49e4-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="b49e4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b49e4-115">Remarks</span></span>

<span data-ttu-id="b49e4-116">Ниже приведены сводные сведения об использовании параметров *wParam* и *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b49e4-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="b49e4-117">Источник сообщения</span><span class="sxs-lookup"><span data-stu-id="b49e4-117">Message Source</span></span> | <span data-ttu-id="b49e4-118">wParam (высокое слово)</span><span class="sxs-lookup"><span data-stu-id="b49e4-118">wParam (high word)</span></span>                | <span data-ttu-id="b49e4-119">wParam (низкое слово)</span><span class="sxs-lookup"><span data-stu-id="b49e4-119">wParam (low word)</span></span>                | <span data-ttu-id="b49e4-120">lParam</span><span class="sxs-lookup"><span data-stu-id="b49e4-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="b49e4-121">Меню</span><span class="sxs-lookup"><span data-stu-id="b49e4-121">Menu</span></span>           | <span data-ttu-id="b49e4-122">0</span><span class="sxs-lookup"><span data-stu-id="b49e4-122">0</span></span>                                 | <span data-ttu-id="b49e4-123">Идентификатор меню (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="b49e4-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="b49e4-124">0</span><span class="sxs-lookup"><span data-stu-id="b49e4-124">0</span></span>                            |
| <span data-ttu-id="b49e4-125">Accelerator</span><span class="sxs-lookup"><span data-stu-id="b49e4-125">Accelerator</span></span>    | <span data-ttu-id="b49e4-126">1</span><span class="sxs-lookup"><span data-stu-id="b49e4-126">1</span></span>                                 | <span data-ttu-id="b49e4-127">Идентификатор ускорителя (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="b49e4-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="b49e4-128">0</span><span class="sxs-lookup"><span data-stu-id="b49e4-128">0</span></span>                            |
| <span data-ttu-id="b49e4-129">Control</span><span class="sxs-lookup"><span data-stu-id="b49e4-129">Control</span></span>        | <span data-ttu-id="b49e4-130">Код уведомления, определяемый элементом управления</span><span class="sxs-lookup"><span data-stu-id="b49e4-130">Control-defined notification code</span></span> | <span data-ttu-id="b49e4-131">Идентификатор элемента управления</span><span class="sxs-lookup"><span data-stu-id="b49e4-131">Control identifier</span></span>               | <span data-ttu-id="b49e4-132">Маркер окна управления</span><span class="sxs-lookup"><span data-stu-id="b49e4-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="b49e4-133">Меню</span><span class="sxs-lookup"><span data-stu-id="b49e4-133">Menus</span></span>

<span data-ttu-id="b49e4-134">Если приложение включает разделитель меню, система отправляет **\_ командное сообщение WM** с младшим словом параметра *wParam* , установленным в ноль, когда пользователь выбирает разделитель.</span><span class="sxs-lookup"><span data-stu-id="b49e4-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="b49e4-135">Если меню определено со значением [**менуинфо. Двстиле**](/windows/win32/api/winuser/ns-winuser-menuinfo) **MNS \_ нотифибипос**, то вместо **\_ команды WM** отправляется [**WM \_ MENUCOMMAND**](wm-menucommand.md) .</span><span class="sxs-lookup"><span data-stu-id="b49e4-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="b49e4-136">Клавиши быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="b49e4-136">Accelerators</span></span>

<span data-ttu-id="b49e4-137">Нажатия клавиш быстрого вызова, которые выбирают элементы из меню окно, преобразуются в сообщения [**WM \_ сискомманд**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="b49e4-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="b49e4-138">Если нажатие клавиши быстрого вызова соответствует пункту меню, когда окно, которому принадлежит меню, является сведенным, то **\_ командное сообщение WM** не отправляется.</span><span class="sxs-lookup"><span data-stu-id="b49e4-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="b49e4-139">Однако если нажатие клавиши быстрого вызова не соответствует ни одному из элементов в меню окна или меню окна, отправляется **\_ командное сообщение WM** , даже если окно является сведенным.</span><span class="sxs-lookup"><span data-stu-id="b49e4-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49e4-140">Требования</span><span class="sxs-lookup"><span data-stu-id="b49e4-140">Requirements</span></span>



| <span data-ttu-id="b49e4-141">Требование</span><span class="sxs-lookup"><span data-stu-id="b49e4-141">Requirement</span></span> | <span data-ttu-id="b49e4-142">Значение</span><span class="sxs-lookup"><span data-stu-id="b49e4-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49e4-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b49e4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b49e4-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b49e4-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b49e4-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b49e4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b49e4-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b49e4-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b49e4-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b49e4-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49e4-148"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b49e4-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49e4-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b49e4-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="b49e4-150">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b49e4-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="b49e4-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b49e4-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b49e4-152">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b49e4-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b49e4-153">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b49e4-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b49e4-154">Меню</span><span class="sxs-lookup"><span data-stu-id="b49e4-154">Menus</span></span>](menus.md)
</dt> </dl>

 

