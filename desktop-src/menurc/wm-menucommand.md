---
title: Сообщение WM_MENUCOMMAND (Winuser. h)
description: Посылается, когда пользователь делает выбор из меню.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416153"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="ae80d-104">\_Сообщение MENUCOMMAND WM</span><span class="sxs-lookup"><span data-stu-id="ae80d-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="ae80d-105">Посылается, когда пользователь делает выбор из меню.</span><span class="sxs-lookup"><span data-stu-id="ae80d-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="ae80d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae80d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae80d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae80d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae80d-108">Отсчитываемый от нуля индекс выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="ae80d-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="ae80d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae80d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae80d-110">Маркер меню для выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="ae80d-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae80d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae80d-111">Remarks</span></span>

<span data-ttu-id="ae80d-112">Сообщение **WM \_ MENUCOMMAND** предоставляет в меню указатель, позволяющий получить доступ к данным меню в структуре [**менуинфо**](/windows/win32/api/winuser/ns-winuser-menuinfo) , а также предоставляет индекс выбранного элемента, который обычно требуется приложениям.</span><span class="sxs-lookup"><span data-stu-id="ae80d-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="ae80d-113">В отличие от этого [**, \_ командное сообщение WM**](wm-command.md) предоставляет идентификатор пункта меню.</span><span class="sxs-lookup"><span data-stu-id="ae80d-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="ae80d-114">Сообщение **WM \_ MENUCOMMAND** отправляется только для меню, определенных флагом **MNS \_ нотифибипос** , установленным в элементе **двстиле** структуры [**менуинфо**](/windows/win32/api/winuser/ns-winuser-menuinfo) .</span><span class="sxs-lookup"><span data-stu-id="ae80d-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae80d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ae80d-115">Requirements</span></span>



| <span data-ttu-id="ae80d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ae80d-116">Requirement</span></span> | <span data-ttu-id="ae80d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ae80d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae80d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae80d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae80d-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ae80d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ae80d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae80d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae80d-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ae80d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae80d-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ae80d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae80d-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae80d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae80d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae80d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae80d-125">Общие сведения о меню</span><span class="sxs-lookup"><span data-stu-id="ae80d-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





