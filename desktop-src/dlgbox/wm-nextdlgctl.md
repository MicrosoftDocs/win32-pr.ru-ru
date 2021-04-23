---
title: Сообщение WM_NEXTDLGCTL (Winuser. h)
description: Отправляется в процедуру диалогового окна, чтобы установить фокус клавиатуры на другой элемент управления в диалоговом окне.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534730"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="29943-104">\_Сообщение НЕКСТДЛГКТЛ WM</span><span class="sxs-lookup"><span data-stu-id="29943-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="29943-105">Отправляется в процедуру диалогового окна, чтобы установить фокус клавиатуры на другой элемент управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="29943-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="29943-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29943-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29943-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29943-108">Если значение *lParam* равно **true**, этот параметр определяет элемент управления, который получает фокус.</span><span class="sxs-lookup"><span data-stu-id="29943-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="29943-109">Если значение *lParam* равно **false**, этот параметр указывает, получает ли фокус следующий или предыдущий элемент управления со стилем **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="29943-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="29943-110">Если параметр *wParam* равен нулю, следующий элемент управления получает фокус; в противном случае фокус получает предыдущий элемент управления с стилем **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="29943-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="29943-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29943-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29943-112">Слово нижнего порядка указывает, как система использует *wParam*.</span><span class="sxs-lookup"><span data-stu-id="29943-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="29943-113">Если слово низкого порядка имеет **значение true**, то параметр *wParam* является маркером, связанным с элементом управления, который получает фокус. в противном случае *wParam* — это флаг, указывающий, получает ли фокус следующий или предыдущий элемент управления со стилем **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="29943-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29943-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29943-114">Return value</span></span>

<span data-ttu-id="29943-115">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="29943-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="29943-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29943-116">Remarks</span></span>

<span data-ttu-id="29943-117">Это сообщение выполняет дополнительные операции управления диалогового окна, помимо тех, которые выполняются функцией [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) . **\_ некстдлгктл** обновляет границу кнопки по умолчанию, устанавливает идентификатор элемента управления по умолчанию и автоматически выбирает текст элемента управления "поле ввода" (если целевое окно является элементом управления редактирования).</span><span class="sxs-lookup"><span data-stu-id="29943-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="29943-118">Не используйте функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) для отправки сообщения **WM \_ некстдлгктл** , если приложение будет параллельно обрабатывать другие сообщения, которые задают фокус.</span><span class="sxs-lookup"><span data-stu-id="29943-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="29943-119">Вместо этого используйте функцию [**посообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="29943-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="29943-120">Требования</span><span class="sxs-lookup"><span data-stu-id="29943-120">Requirements</span></span>



| <span data-ttu-id="29943-121">Требование</span><span class="sxs-lookup"><span data-stu-id="29943-121">Requirement</span></span> | <span data-ttu-id="29943-122">Значение</span><span class="sxs-lookup"><span data-stu-id="29943-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29943-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29943-123">Minimum supported client</span></span><br/> | <span data-ttu-id="29943-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29943-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="29943-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29943-125">Minimum supported server</span></span><br/> | <span data-ttu-id="29943-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29943-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29943-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29943-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="29943-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29943-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29943-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29943-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="29943-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="29943-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29943-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="29943-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="29943-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="29943-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="29943-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="29943-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="29943-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="29943-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29943-135">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="29943-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

