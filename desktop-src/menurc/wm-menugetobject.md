---
title: Сообщение WM_MENUGETOBJECT (Winuser. h)
description: Посылается владельцу меню перетаскивания, когда курсор мыши попадает в пункт меню или перемещается от центра элемента к верхнему или нижнему краю элемента.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535552"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="14bc7-104">\_Сообщение МЕНУЖЕТОБЖЕКТ WM</span><span class="sxs-lookup"><span data-stu-id="14bc7-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="14bc7-105">Посылается владельцу меню перетаскивания, когда курсор мыши попадает в пункт меню или перемещается от центра элемента к верхнему или нижнему краю элемента.</span><span class="sxs-lookup"><span data-stu-id="14bc7-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="14bc7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14bc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14bc7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14bc7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14bc7-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="14bc7-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="14bc7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14bc7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14bc7-110">Указатель на структуру [**менужетобжектинфо**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .</span><span class="sxs-lookup"><span data-stu-id="14bc7-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14bc7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14bc7-111">Return value</span></span>

<span data-ttu-id="14bc7-112">Приложение должно вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="14bc7-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="14bc7-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="14bc7-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="14bc7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="14bc7-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14bc7-115"><dt>**МНГО \_ Ошибка**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="14bc7-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="14bc7-116">В элементе **пвобж** элемента [**менужетобжектинфо**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) был возвращен указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14bc7-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="14bc7-117"><dt>**МНГО \_ Интерфейс неинтерфейса**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="14bc7-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="14bc7-118">Интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="14bc7-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="14bc7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="14bc7-119">Requirements</span></span>



| <span data-ttu-id="14bc7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="14bc7-120">Requirement</span></span> | <span data-ttu-id="14bc7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="14bc7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bc7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14bc7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14bc7-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14bc7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="14bc7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14bc7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14bc7-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14bc7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14bc7-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14bc7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="14bc7-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14bc7-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14bc7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14bc7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bc7-129">Общие сведения о меню</span><span class="sxs-lookup"><span data-stu-id="14bc7-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





