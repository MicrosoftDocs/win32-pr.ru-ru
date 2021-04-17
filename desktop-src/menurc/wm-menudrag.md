---
title: Сообщение WM_MENUDRAG (Winuser. h)
description: Посылается владельцу меню перетаскивания, когда пользователь перетаскивает элемент меню.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710556"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="c1f85-104">\_Сообщение МЕНУДРАГ WM</span><span class="sxs-lookup"><span data-stu-id="c1f85-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="c1f85-105">Посылается владельцу меню перетаскивания, когда пользователь перетаскивает элемент меню.</span><span class="sxs-lookup"><span data-stu-id="c1f85-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="c1f85-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1f85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1f85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1f85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1f85-108">Позиция элемента, с которого началась операция перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="c1f85-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="c1f85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1f85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1f85-110">Маркер меню, содержащего элемент.</span><span class="sxs-lookup"><span data-stu-id="c1f85-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1f85-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1f85-111">Return value</span></span>

<span data-ttu-id="c1f85-112">Приложение должно вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c1f85-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="c1f85-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c1f85-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="c1f85-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c1f85-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1f85-115"><dt>**МНД \_ ПРОДОЛЖИТЬ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c1f85-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c1f85-116">Меню должно оставаться активным.</span><span class="sxs-lookup"><span data-stu-id="c1f85-116">Menu should remain active.</span></span> <span data-ttu-id="c1f85-117">Если мышь освобождена, ее следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="c1f85-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="c1f85-118"><dt>**МНД \_ ЕНДМЕНУ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c1f85-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="c1f85-119">Меню должно быть завершено.</span><span class="sxs-lookup"><span data-stu-id="c1f85-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="c1f85-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1f85-120">Remarks</span></span>

<span data-ttu-id="c1f85-121">Приложение может вызвать функцию [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="c1f85-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="c1f85-122">Чтобы создать меню перетаскивания, вызовите [**сетменуинфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) с помощью **MNS \_ DRAGDROP**.</span><span class="sxs-lookup"><span data-stu-id="c1f85-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1f85-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c1f85-123">Requirements</span></span>



| <span data-ttu-id="c1f85-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c1f85-124">Requirement</span></span> | <span data-ttu-id="c1f85-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c1f85-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f85-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1f85-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f85-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1f85-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1f85-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1f85-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f85-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1f85-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1f85-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1f85-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1f85-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1f85-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1f85-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1f85-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1f85-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c1f85-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1f85-134">**сетменуинфо**</span><span class="sxs-lookup"><span data-stu-id="c1f85-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="c1f85-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c1f85-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1f85-136">Меню</span><span class="sxs-lookup"><span data-stu-id="c1f85-136">Menus</span></span>](menus.md)
</dt> </dl>

 

