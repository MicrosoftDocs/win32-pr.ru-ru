---
title: Сообщение WM_SETHOTKEY (Winuser. h)
description: Отправляется в окно для связывания горячих клавиш с окном. Когда пользователь нажимает клавишу горячего ключа, система активирует окно.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "103820373"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="81665-105">\_Сообщение СЕСОТКЭЙ WM</span><span class="sxs-lookup"><span data-stu-id="81665-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="81665-106">Отправляется в окно для связывания горячих клавиш с окном.</span><span class="sxs-lookup"><span data-stu-id="81665-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="81665-107">Когда пользователь нажимает клавишу горячего ключа, система активирует окно.</span><span class="sxs-lookup"><span data-stu-id="81665-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="81665-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81665-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81665-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81665-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81665-110">Слово нижнего порядка указывает код виртуального ключа, связываемый с окном.</span><span class="sxs-lookup"><span data-stu-id="81665-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="81665-111">Слово с высоким порядковым значением может быть одним или несколькими из следующих значений в Коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="81665-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="81665-112">При установке параметра *wParam* в **значение NULL** удаляется горячая клавиша, связанная с окном.</span><span class="sxs-lookup"><span data-stu-id="81665-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="81665-113">Значение</span><span class="sxs-lookup"><span data-stu-id="81665-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="81665-114">Значение</span><span class="sxs-lookup"><span data-stu-id="81665-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="81665-115"><dt>**Хоткэйф \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="81665-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="81665-116">ALT - клавиша</span><span class="sxs-lookup"><span data-stu-id="81665-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="81665-117"><dt>**Хоткэйф \_ Управление**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="81665-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="81665-118">Клавиша CTRL</span><span class="sxs-lookup"><span data-stu-id="81665-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="81665-119"><dt>**Хоткэйф \_ EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="81665-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="81665-120">Расширенный ключ</span><span class="sxs-lookup"><span data-stu-id="81665-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="81665-121"><dt>**Хоткэйф \_ SHIFT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="81665-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="81665-122">Клавиша SHIFT</span><span class="sxs-lookup"><span data-stu-id="81665-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="81665-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81665-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81665-124">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="81665-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81665-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81665-125">Return value</span></span>

<span data-ttu-id="81665-126">Возвращаемое значение является одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="81665-126">The return value is one of the following.</span></span>



| <span data-ttu-id="81665-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81665-127">Return value</span></span>                                                                  | <span data-ttu-id="81665-128">Описание</span><span class="sxs-lookup"><span data-stu-id="81665-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81665-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="81665-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="81665-130">Функция не выполнена; Недопустимый горячая клавиша.</span><span class="sxs-lookup"><span data-stu-id="81665-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="81665-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="81665-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="81665-132">Функция не выполнена; Недопустимое окно.</span><span class="sxs-lookup"><span data-stu-id="81665-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="81665-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="81665-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="81665-134">Функция выполнена успешно, и никакие другие окна не имеют такой же горячей клавиши.</span><span class="sxs-lookup"><span data-stu-id="81665-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="81665-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="81665-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="81665-136">Функция выполнена успешно, но другое окно уже имеет ту же горячую клавишу.</span><span class="sxs-lookup"><span data-stu-id="81665-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81665-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81665-137">Remarks</span></span>

<span data-ttu-id="81665-138">Горячая клавиша не может быть связана с дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="81665-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="81665-139">**VK \_** Клавиши Escape **, \_ VK** и **VK являются \_** недопустимыми сочетаниями клавиш.</span><span class="sxs-lookup"><span data-stu-id="81665-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="81665-140">Когда пользователь нажимает сочетание клавиш, система создает сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) с параметром *wParam* , равным **\_ сочетанию клавиш SC** и *lParam* , равным маркеру окна.</span><span class="sxs-lookup"><span data-stu-id="81665-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="81665-141">Если это сообщение передается в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), система переместит Последнее активное всплывающее окно окна (если оно существует) или само окно (если всплывающее окно отсутствует) на передний план.</span><span class="sxs-lookup"><span data-stu-id="81665-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="81665-142">Окно может иметь только одну горячую клавишу.</span><span class="sxs-lookup"><span data-stu-id="81665-142">A window can only have one hot key.</span></span> <span data-ttu-id="81665-143">Если с окном уже связано сочетание клавиш, новый горячая клавиша заменяется на старый.</span><span class="sxs-lookup"><span data-stu-id="81665-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="81665-144">Если в нескольких окнах есть одна и та же горячая клавиша, окно, активируемое горячим ключом, является случайным.</span><span class="sxs-lookup"><span data-stu-id="81665-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="81665-145">Эти Горячие ключи не связаны с горячими ключами, установленными [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span><span class="sxs-lookup"><span data-stu-id="81665-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="81665-146">Требования</span><span class="sxs-lookup"><span data-stu-id="81665-146">Requirements</span></span>



| <span data-ttu-id="81665-147">Требование</span><span class="sxs-lookup"><span data-stu-id="81665-147">Requirement</span></span> | <span data-ttu-id="81665-148">Значение</span><span class="sxs-lookup"><span data-stu-id="81665-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81665-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81665-149">Minimum supported client</span></span><br/> | <span data-ttu-id="81665-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81665-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="81665-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81665-151">Minimum supported server</span></span><br/> | <span data-ttu-id="81665-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81665-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81665-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="81665-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="81665-154"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81665-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81665-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81665-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="81665-156">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="81665-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81665-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="81665-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="81665-158">**\_сочетание клавиш WM**</span><span class="sxs-lookup"><span data-stu-id="81665-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="81665-159">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="81665-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="81665-160">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="81665-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81665-161">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="81665-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

