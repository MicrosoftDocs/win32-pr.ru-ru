---
title: Сообщение WM_SETFOCUS (Winuser. h)
description: Посылается окну после того, как оно получило фокус клавиатуры.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492651"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="1e9df-104">\_Сообщение SETFOCUS WM</span><span class="sxs-lookup"><span data-stu-id="1e9df-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="1e9df-105">Посылается окну после того, как оно получило фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="1e9df-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="1e9df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e9df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e9df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9df-108">Маркер окна, которое потеряло фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="1e9df-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="1e9df-109">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e9df-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1e9df-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e9df-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9df-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1e9df-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9df-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e9df-112">Return value</span></span>

<span data-ttu-id="1e9df-113">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="1e9df-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e9df-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e9df-114">Remarks</span></span>

<span data-ttu-id="1e9df-115">Чтобы отобразить курсор, приложение должно вызвать соответствующие функции курсора при получении сообщения **WM \_ SETFOCUS** .</span><span class="sxs-lookup"><span data-stu-id="1e9df-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9df-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1e9df-116">Requirements</span></span>



| <span data-ttu-id="1e9df-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1e9df-117">Requirement</span></span> | <span data-ttu-id="1e9df-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1e9df-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9df-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e9df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9df-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e9df-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1e9df-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e9df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9df-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e9df-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e9df-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e9df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e9df-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e9df-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9df-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e9df-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e9df-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1e9df-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e9df-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="1e9df-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="1e9df-128">**WM \_ киллфокус**</span><span class="sxs-lookup"><span data-stu-id="1e9df-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="1e9df-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1e9df-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e9df-130">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="1e9df-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

