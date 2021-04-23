---
title: Сообщение WM_CTLCOLORDLG (Winuser. h)
description: Отправляется в диалоговое окно до того, как система порисует диалоговое окно. При ответе на это сообщение диалоговое окно может задать цвет текста и фона с помощью указанного маркера контекста отображаемого устройства.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801265"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="4cc0a-105">\_Сообщение КТЛКОЛОРДЛГ WM</span><span class="sxs-lookup"><span data-stu-id="4cc0a-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="4cc0a-106">Отправляется в диалоговое окно до того, как система порисует диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="4cc0a-107">При ответе на это сообщение диалоговое окно может задать цвет текста и фона с помощью указанного маркера контекста отображаемого устройства.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="4cc0a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cc0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc0a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cc0a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cc0a-110">Маркер контекста устройства для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4cc0a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cc0a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cc0a-112">Дескриптор диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc0a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cc0a-113">Return value</span></span>

<span data-ttu-id="4cc0a-114">Если приложение обрабатывает это сообщение, оно должно возвращать маркер кисти.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="4cc0a-115">Система использует кисть для рисования фона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc0a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cc0a-116">Remarks</span></span>

<span data-ttu-id="4cc0a-117">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="4cc0a-118">Система не уничтожает возвращенную кисть автоматически.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="4cc0a-119">Это обязанность приложения для уничтожения кисти, когда она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="4cc0a-120">Сообщение **WM \_ ктлколордлг** никогда не передается между потоками.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="4cc0a-121">Он отправляется только в пределах одного потока.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-121">It is sent only within one thread.</span></span>

<span data-ttu-id="4cc0a-122">Обратите внимание, что сообщение **WM \_ ктлколордлг** отправляется в само диалоговое окно; все остальные сообщения \*\* \_ WM \* ктлколор\* _ отправляются владельцу элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="4cc0a-123">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу _ *int \_ ptr*\* и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="4cc0a-124">Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="4cc0a-125">Значение **\_ мсгресулт DWL** , заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4cc0a-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc0a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4cc0a-126">Requirements</span></span>



| <span data-ttu-id="4cc0a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4cc0a-127">Requirement</span></span> | <span data-ttu-id="4cc0a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4cc0a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc0a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cc0a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc0a-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cc0a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4cc0a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cc0a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc0a-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cc0a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4cc0a-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4cc0a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cc0a-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc0a-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc0a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cc0a-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="4cc0a-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4cc0a-137">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="4cc0a-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="4cc0a-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4cc0a-140">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="4cc0a-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="4cc0a-141">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4cc0a-142">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="4cc0a-143">**селектпалетте**</span><span class="sxs-lookup"><span data-stu-id="4cc0a-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

