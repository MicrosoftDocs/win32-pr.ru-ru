---
title: Сообщение WM_ENTERMENULOOP (Winuser. h)
description: Сообщает процедуре главного окна приложения о том, что был введен модальный цикл меню.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710459"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="1885b-104">\_Сообщение ЕНТЕРМЕНУЛУП WM</span><span class="sxs-lookup"><span data-stu-id="1885b-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="1885b-105">Сообщает процедуре главного окна приложения о том, что был введен модальный цикл меню.</span><span class="sxs-lookup"><span data-stu-id="1885b-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="1885b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1885b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1885b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1885b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1885b-108">Указывает, было ли указано меню "окно" с помощью функции [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) .</span><span class="sxs-lookup"><span data-stu-id="1885b-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="1885b-109">Этот параметр имеет значение **true** , если меню окна было указано с помощью **метод TrackPopupMenu**, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1885b-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="1885b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1885b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1885b-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1885b-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1885b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1885b-112">Return value</span></span>

<span data-ttu-id="1885b-113">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="1885b-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1885b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1885b-114">Remarks</span></span>

<span data-ttu-id="1885b-115">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1885b-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1885b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1885b-116">Requirements</span></span>



| <span data-ttu-id="1885b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1885b-117">Requirement</span></span> | <span data-ttu-id="1885b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1885b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1885b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1885b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1885b-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1885b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1885b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1885b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1885b-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1885b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1885b-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1885b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1885b-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1885b-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1885b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1885b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1885b-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1885b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1885b-127">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="1885b-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1885b-128">**WM \_ екситменулуп**</span><span class="sxs-lookup"><span data-stu-id="1885b-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="1885b-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1885b-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1885b-130">Меню</span><span class="sxs-lookup"><span data-stu-id="1885b-130">Menus</span></span>](menus.md)
</dt> </dl>

 

