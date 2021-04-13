---
title: Сообщение WM_MENURBUTTONUP (Winuser. h)
description: Посылается, когда пользователь отпускает правую кнопку мыши, когда курсор находится над пунктом меню.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341350"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="b1088-104">\_Сообщение МЕНУРБУТТОНУП WM</span><span class="sxs-lookup"><span data-stu-id="b1088-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="b1088-105">Посылается, когда пользователь отпускает правую кнопку мыши, когда курсор находится над пунктом меню.</span><span class="sxs-lookup"><span data-stu-id="b1088-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="b1088-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1088-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1088-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1088-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1088-108">Отсчитываемый от нуля индекс элемента меню, в котором была отжата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="b1088-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="b1088-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1088-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1088-110">Маркер меню, содержащего элемент.</span><span class="sxs-lookup"><span data-stu-id="b1088-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1088-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1088-111">Remarks</span></span>

<span data-ttu-id="b1088-112">Сообщение **WM \_ менурбуттонуп** позволяет приложениям предоставлять контекстно-зависимое меню, которое также называется контекстным меню для пункта меню, указанного в этом сообщении.</span><span class="sxs-lookup"><span data-stu-id="b1088-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="b1088-113">Чтобы отобразить контекстное меню для пункта меню, вызовите функцию [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) с **\_ рекурсией TPM**.</span><span class="sxs-lookup"><span data-stu-id="b1088-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1088-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b1088-114">Requirements</span></span>



| <span data-ttu-id="b1088-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b1088-115">Requirement</span></span> | <span data-ttu-id="b1088-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b1088-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1088-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1088-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1088-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1088-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1088-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1088-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1088-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1088-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1088-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b1088-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1088-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1088-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1088-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1088-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1088-124">Общие сведения о меню</span><span class="sxs-lookup"><span data-stu-id="b1088-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





