---
title: Сообщение WM_GETHOTKEY (Winuser. h)
description: Отправлено, чтобы определить горячую клавишу, связанную с окном.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- WM_GETHOTKEY ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490050"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="5f408-104">Сообщение WM с \_ сочетанием клавиш</span><span class="sxs-lookup"><span data-stu-id="5f408-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="5f408-105">Отправлено, чтобы определить горячую клавишу, связанную с окном.</span><span class="sxs-lookup"><span data-stu-id="5f408-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="5f408-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f408-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f408-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f408-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5f408-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f408-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f408-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f408-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5f408-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f408-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f408-111">Return value</span></span>

<span data-ttu-id="5f408-112">Возвращаемое значение — это код виртуального ключа и модификаторы для сочетания клавиш, или **значение NULL** , если с окном не связана ни одна горячая клавиша.</span><span class="sxs-lookup"><span data-stu-id="5f408-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="5f408-113">Код виртуального ключа находится в младшем байте возвращаемого значения, а модификаторы — в высоком байте.</span><span class="sxs-lookup"><span data-stu-id="5f408-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="5f408-114">Модификаторы могут быть сочетанием следующих флагов из Коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="5f408-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="5f408-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="5f408-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="5f408-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5f408-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="5f408-117"><dt>**Хоткэйф \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="5f408-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="5f408-118">ALT - клавиша</span><span class="sxs-lookup"><span data-stu-id="5f408-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="5f408-119"><dt>**Хоткэйф \_ Управление**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="5f408-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="5f408-120">Клавиша CTRL</span><span class="sxs-lookup"><span data-stu-id="5f408-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="5f408-121"><dt>**Хоткэйф \_ EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="5f408-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="5f408-122">Расширенный ключ</span><span class="sxs-lookup"><span data-stu-id="5f408-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="5f408-123"><dt>**Хоткэйф \_ SHIFT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="5f408-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="5f408-124">Клавиша SHIFT</span><span class="sxs-lookup"><span data-stu-id="5f408-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="5f408-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f408-125">Remarks</span></span>

<span data-ttu-id="5f408-126">Эти горячие клавиши не связаны с горячими ключами, заданными функцией [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .</span><span class="sxs-lookup"><span data-stu-id="5f408-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f408-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5f408-127">Requirements</span></span>



| <span data-ttu-id="5f408-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5f408-128">Requirement</span></span> | <span data-ttu-id="5f408-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5f408-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f408-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f408-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5f408-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f408-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5f408-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f408-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5f408-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f408-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f408-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5f408-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f408-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f408-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f408-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f408-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f408-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5f408-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f408-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="5f408-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="5f408-139">**WM \_ сесоткэй**</span><span class="sxs-lookup"><span data-stu-id="5f408-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="5f408-140">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5f408-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f408-141">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="5f408-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

