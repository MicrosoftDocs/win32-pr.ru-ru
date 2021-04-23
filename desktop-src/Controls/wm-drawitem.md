---
title: Сообщение WM_DRAWITEM (Winuser. h)
description: Посылается родительскому окну рисуемой владельцем кнопки, поля со списком, списка или меню при изменении визуального элемента кнопки, поля со списком, списка или меню.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Элементы управления Windows для WM_DRAWITEM сообщений
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802171"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="f464a-104">\_Сообщение DRAWITEM WM</span><span class="sxs-lookup"><span data-stu-id="f464a-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="f464a-105">Посылается родительскому окну рисуемой владельцем кнопки, поля со списком, списка или меню при изменении визуального элемента кнопки, поля со списком, списка или меню.</span><span class="sxs-lookup"><span data-stu-id="f464a-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="f464a-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f464a-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f464a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f464a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f464a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f464a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f464a-109">Указывает идентификатор элемента управления, который отправил сообщение **WM \_ DRAWITEM** .</span><span class="sxs-lookup"><span data-stu-id="f464a-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="f464a-110">Если сообщение было отправлено меню, этот параметр равен нулю.</span><span class="sxs-lookup"><span data-stu-id="f464a-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="f464a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f464a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f464a-112">Указатель на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , содержащую сведения о рисуемом элементе, и требуемый тип рисования.</span><span class="sxs-lookup"><span data-stu-id="f464a-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f464a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f464a-113">Return value</span></span>

<span data-ttu-id="f464a-114">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f464a-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f464a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f464a-115">Remarks</span></span>

<span data-ttu-id="f464a-116">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) рисует прямоугольник фокуса для элемента списка, рисуемого владельцем.</span><span class="sxs-lookup"><span data-stu-id="f464a-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="f464a-117">Элемент *итемактион* структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) указывает операцию рисования, которую должно выполнить приложение.</span><span class="sxs-lookup"><span data-stu-id="f464a-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="f464a-118">Перед возвратом из обработки этого сообщения приложение должно убедиться, что контекст устройства, определенный членом *HDC* структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , находится в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f464a-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f464a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f464a-119">Requirements</span></span>



| <span data-ttu-id="f464a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f464a-120">Requirement</span></span> | <span data-ttu-id="f464a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f464a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f464a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f464a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f464a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f464a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f464a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f464a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f464a-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f464a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f464a-126">Header</span><span class="sxs-lookup"><span data-stu-id="f464a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f464a-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f464a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f464a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f464a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f464a-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f464a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f464a-130">**дравитемструкт**</span><span class="sxs-lookup"><span data-stu-id="f464a-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="f464a-131">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="f464a-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f464a-132">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="f464a-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

