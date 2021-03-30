---
title: Сообщение WM_INITMENUPOPUP (Winuser. h)
description: Посылается, когда раскрывающееся меню или подменю станет активным. Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071340"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="79673-105">\_Сообщение ИНИТМЕНУПОПУП WM</span><span class="sxs-lookup"><span data-stu-id="79673-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="79673-106">Посылается, когда раскрывающееся меню или подменю станет активным.</span><span class="sxs-lookup"><span data-stu-id="79673-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="79673-107">Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.</span><span class="sxs-lookup"><span data-stu-id="79673-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="79673-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79673-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79673-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79673-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79673-110">Маркер раскрывающегося меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="79673-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="79673-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79673-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79673-112">Слово нижнего порядка указывает относительное расположение элемента меню, начинающееся с нуля, которое открывает раскрывающееся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="79673-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="79673-113">Слово высокого порядка указывает, является ли раскрывающееся меню окном.</span><span class="sxs-lookup"><span data-stu-id="79673-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="79673-114">Если меню является меню окно, этот параметр имеет **значение true**; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="79673-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79673-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79673-115">Return value</span></span>

<span data-ttu-id="79673-116">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="79673-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="79673-117">Требования</span><span class="sxs-lookup"><span data-stu-id="79673-117">Requirements</span></span>



| <span data-ttu-id="79673-118">Требование</span><span class="sxs-lookup"><span data-stu-id="79673-118">Requirement</span></span> | <span data-ttu-id="79673-119">Значение</span><span class="sxs-lookup"><span data-stu-id="79673-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79673-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79673-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79673-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79673-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="79673-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79673-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79673-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79673-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79673-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="79673-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79673-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79673-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79673-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79673-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="79673-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="79673-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="79673-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79673-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="79673-129">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79673-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="79673-130">**WM \_ инитмену**</span><span class="sxs-lookup"><span data-stu-id="79673-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="79673-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="79673-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="79673-132">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="79673-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

