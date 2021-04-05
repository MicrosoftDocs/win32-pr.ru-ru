---
title: Сообщение WM_EXITMENULOOP (Winuser. h)
description: Сообщает процедуре главного окна приложения о том, что был завершен модальный цикл меню.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802429"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="38745-104">\_Сообщение ЕКСИТМЕНУЛУП WM</span><span class="sxs-lookup"><span data-stu-id="38745-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="38745-105">Сообщает процедуре главного окна приложения о том, что был завершен модальный цикл меню.</span><span class="sxs-lookup"><span data-stu-id="38745-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="38745-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38745-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38745-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38745-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38745-108">Указывает, является ли меню контекстным меню.</span><span class="sxs-lookup"><span data-stu-id="38745-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="38745-109">Этот параметр имеет значение **true** , если это контекстное меню, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="38745-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="38745-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38745-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38745-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="38745-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38745-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38745-112">Return value</span></span>

<span data-ttu-id="38745-113">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="38745-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="38745-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38745-114">Remarks</span></span>

<span data-ttu-id="38745-115">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="38745-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="38745-116">Требования</span><span class="sxs-lookup"><span data-stu-id="38745-116">Requirements</span></span>



| <span data-ttu-id="38745-117">Требование</span><span class="sxs-lookup"><span data-stu-id="38745-117">Requirement</span></span> | <span data-ttu-id="38745-118">Значение</span><span class="sxs-lookup"><span data-stu-id="38745-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38745-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38745-119">Minimum supported client</span></span><br/> | <span data-ttu-id="38745-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38745-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38745-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38745-121">Minimum supported server</span></span><br/> | <span data-ttu-id="38745-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38745-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38745-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="38745-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="38745-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38745-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38745-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38745-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="38745-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="38745-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38745-127">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="38745-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="38745-128">**WM \_ ентерменулуп**</span><span class="sxs-lookup"><span data-stu-id="38745-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="38745-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="38745-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38745-130">Меню</span><span class="sxs-lookup"><span data-stu-id="38745-130">Menus</span></span>](menus.md)
</dt> </dl>

 

