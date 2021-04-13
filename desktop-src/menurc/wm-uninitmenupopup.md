---
title: Сообщение WM_UNINITMENUPOPUP (Winuser. h)
description: Посылается при уничтожении раскрывающегося меню или подменю.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535543"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="2a751-104">\_Сообщение УНИНИТМЕНУПОПУП WM</span><span class="sxs-lookup"><span data-stu-id="2a751-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="2a751-105">Посылается при уничтожении раскрывающегося меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="2a751-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="2a751-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a751-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a751-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a751-108">Маркер меню</span><span class="sxs-lookup"><span data-stu-id="2a751-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="2a751-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a751-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a751-110">Слово в высоком порядке указывает на удаленное меню.</span><span class="sxs-lookup"><span data-stu-id="2a751-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="2a751-111">В настоящее время этот параметр может иметь только значение **MF \_ сисмену** (меню "окно").</span><span class="sxs-lookup"><span data-stu-id="2a751-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a751-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a751-112">Remarks</span></span>

<span data-ttu-id="2a751-113">Если приложение получает сообщение [**WM \_ инитменупопуп**](wm-initmenupopup.md) , оно получит сообщение **WM \_ унинитменупопуп** .</span><span class="sxs-lookup"><span data-stu-id="2a751-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a751-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2a751-114">Requirements</span></span>



| <span data-ttu-id="2a751-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2a751-115">Requirement</span></span> | <span data-ttu-id="2a751-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2a751-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a751-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a751-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a751-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a751-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2a751-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a751-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a751-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a751-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a751-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2a751-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a751-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a751-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a751-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a751-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a751-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2a751-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="2a751-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a751-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2a751-126">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2a751-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a751-127">Меню</span><span class="sxs-lookup"><span data-stu-id="2a751-127">Menus</span></span>](menus.md)
</dt> </dl>

 

