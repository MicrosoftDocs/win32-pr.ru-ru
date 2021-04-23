---
title: Сообщение WM_ENTERIDLE (Winuser. h)
description: Отправляется в окно владельца модального диалогового окна или меню, которое переходит в состояние простоя. Модальное диалоговое окно или меню переходит в состояние простоя, если в очереди нет сообщений, ожидающих обработки одного или нескольких предыдущих сообщений.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415912"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="3f3e7-105">\_Сообщение ЕНТЕРИДЛЕ WM</span><span class="sxs-lookup"><span data-stu-id="3f3e7-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="3f3e7-106">Отправляется в окно владельца модального диалогового окна или меню, которое переходит в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="3f3e7-107">Модальное диалоговое окно или меню переходит в состояние простоя, если в очереди нет сообщений, ожидающих обработки одного или нескольких предыдущих сообщений.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="3f3e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f3e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f3e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f3e7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3e7-110">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3f3e7-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3f3e7-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="3f3e7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3f3e7-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="3f3e7-113"><dt>**Мсгф \_ ДИАЛОГБОКС**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3f3e7-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3f3e7-114">Система бездействует, так как отображается диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="3f3e7-115"><dt>**Мсгф \_ МЕНЮ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3f3e7-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="3f3e7-116">Система бездействует, поскольку отображается меню.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="3f3e7-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f3e7-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3e7-118">Маркер диалогового окна (если *wParam* — **мсгф \_ диалогбокс**) или окно, содержащее отображаемое меню (если *wParam* — **мсгф \_ меню**).</span><span class="sxs-lookup"><span data-stu-id="3f3e7-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f3e7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f3e7-119">Return value</span></span>

<span data-ttu-id="3f3e7-120">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f3e7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f3e7-121">Remarks</span></span>

<span data-ttu-id="3f3e7-122">Вы можете отключить сообщение **WM \_ ентеридле** для диалогового окна, создав диалоговое окно с помощью стиля **DS \_ ноидлемсг** .</span><span class="sxs-lookup"><span data-stu-id="3f3e7-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3e7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3f3e7-123">Requirements</span></span>



| <span data-ttu-id="3f3e7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3f3e7-124">Requirement</span></span> | <span data-ttu-id="3f3e7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3f3e7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3e7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f3e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3e7-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f3e7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3f3e7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f3e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3e7-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f3e7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f3e7-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3f3e7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f3e7-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f3e7-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f3e7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f3e7-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f3e7-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3f3e7-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3f3e7-134">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="3f3e7-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="3f3e7-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3f3e7-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3f3e7-136">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="3f3e7-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

