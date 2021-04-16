---
title: Сообщение WM_MENUSELECT (Winuser. h)
description: Отправляется в окно владельца меню, когда пользователь выбирает пункт меню.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710555"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="3d427-104">\_Сообщение МЕНУСЕЛЕКТ WM</span><span class="sxs-lookup"><span data-stu-id="3d427-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="3d427-105">Отправляется в окно владельца меню, когда пользователь выбирает пункт меню.</span><span class="sxs-lookup"><span data-stu-id="3d427-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="3d427-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d427-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d427-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d427-108">Слово нижнего порядка указывает пункт меню или индекс подменю.</span><span class="sxs-lookup"><span data-stu-id="3d427-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="3d427-109">Если выбранный элемент является командным элементом, этот параметр содержит идентификатор элемента меню.</span><span class="sxs-lookup"><span data-stu-id="3d427-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="3d427-110">Если выбранный элемент открывает раскрывающееся меню или подменю, этот параметр содержит индекс раскрывающегося меню или подменю в главном меню, а параметр *lParam* содержит маркер главного меню (щелчок). Используйте функцию [**Menu, чтобы**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) получить маркер меню в раскрывающемся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="3d427-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="3d427-111">Слово в высоком порядке указывает один или несколько флагов меню.</span><span class="sxs-lookup"><span data-stu-id="3d427-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="3d427-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3d427-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3d427-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3d427-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="3d427-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3d427-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="3d427-115"><dt>**MF \_ ТОЧЕЧный рисунок**</dt> <dt>0x00000004L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="3d427-116">Элемент отображает точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="3d427-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="3d427-117"><dt>**MF \_ ПРОВЕРЕНо**</dt> <dt>0x00000008L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="3d427-118">Элемент установлен.</span><span class="sxs-lookup"><span data-stu-id="3d427-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="3d427-119"><dt>**MF \_ ОТКЛЮЧЕНные**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="3d427-120">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="3d427-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="3d427-121"><dt>**MF \_ Несерый**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3d427-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="3d427-122">Элемент является серым.</span><span class="sxs-lookup"><span data-stu-id="3d427-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="3d427-123"><dt>**MF \_ ХИЛИТЕ**</dt> <dt>0x00000080L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="3d427-124">Элемент выделен.</span><span class="sxs-lookup"><span data-stu-id="3d427-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="3d427-125"><dt>**MF \_ МАУСЕСЕЛЕКТ**</dt> <dt>0x00008000L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="3d427-126">Элемент выбран с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="3d427-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="3d427-127"><dt>**MF \_ ОВНЕРДРАВ**</dt> <dt>0x00000100L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="3d427-128">Элемент является рисуемым владельцем элементом.</span><span class="sxs-lookup"><span data-stu-id="3d427-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="3d427-129"><dt>**MF \_ Всплывающее окно**</dt> <dt>0x00000010L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="3d427-130">Элемент открывает раскрывающееся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="3d427-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="3d427-131"><dt>**MF \_ СИСМЕНУ**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="3d427-132">Элемент содержится в меню окно.</span><span class="sxs-lookup"><span data-stu-id="3d427-132">Item is contained in the window menu.</span></span> <span data-ttu-id="3d427-133">Параметр *lParam* содержит маркер для меню, связанного с сообщением.</span><span class="sxs-lookup"><span data-stu-id="3d427-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3d427-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d427-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d427-135">Маркер меню, которое было выбрано.</span><span class="sxs-lookup"><span data-stu-id="3d427-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d427-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d427-136">Return value</span></span>

<span data-ttu-id="3d427-137">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3d427-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d427-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d427-138">Remarks</span></span>

<span data-ttu-id="3d427-139">Если слово « *wParam* » высокого порядка содержит 0xFFFF, а параметр *lParam* содержит **значение NULL**, система закрыла меню.</span><span class="sxs-lookup"><span data-stu-id="3d427-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="3d427-140">Не используйте значение 1 для слова с высоким приоритетом *wParam*, так как это значение указано как (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span><span class="sxs-lookup"><span data-stu-id="3d427-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="3d427-141">Если значение равно 0xFFFF, то оно будет интерпретироваться как 0x0000FFFF, а не как 1, из-за приведения к типу **uint**.</span><span class="sxs-lookup"><span data-stu-id="3d427-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d427-142">Требования</span><span class="sxs-lookup"><span data-stu-id="3d427-142">Requirements</span></span>



| <span data-ttu-id="3d427-143">Требование</span><span class="sxs-lookup"><span data-stu-id="3d427-143">Requirement</span></span> | <span data-ttu-id="3d427-144">Значение</span><span class="sxs-lookup"><span data-stu-id="3d427-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d427-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d427-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3d427-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d427-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d427-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d427-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3d427-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d427-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d427-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3d427-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d427-150"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d427-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d427-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d427-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d427-152">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3d427-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3d427-153">**Вложенное меню**</span><span class="sxs-lookup"><span data-stu-id="3d427-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="3d427-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d427-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3d427-155">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d427-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3d427-156">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3d427-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d427-157">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="3d427-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

