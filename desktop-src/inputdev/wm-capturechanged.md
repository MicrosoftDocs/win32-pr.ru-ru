---
title: Сообщение WM_CAPTURECHANGED (Winuser. h)
description: Отправляется в окно, которое теряет захват мыши.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- WM_CAPTURECHANGED ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135639"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="19999-104">\_Сообщение КАПТУРЕЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="19999-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="19999-105">Отправляется в окно, которое теряет захват мыши.</span><span class="sxs-lookup"><span data-stu-id="19999-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="19999-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19999-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="19999-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="19999-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19999-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19999-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19999-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="19999-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="19999-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19999-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19999-111">Указатель на окно, получив захват мыши.</span><span class="sxs-lookup"><span data-stu-id="19999-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19999-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19999-112">Return value</span></span>

<span data-ttu-id="19999-113">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="19999-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="19999-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19999-114">Remarks</span></span>

<span data-ttu-id="19999-115">Окно получает это сообщение, даже если оно вызывает [**релеасекаптуре**](/windows/win32/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="19999-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="19999-116">Приложение не должно пытаться установить захват мыши в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="19999-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="19999-117">При получении этого сообщения окно должно перерисовывать себя при необходимости, чтобы отразить новое состояние захвата мыши.</span><span class="sxs-lookup"><span data-stu-id="19999-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="19999-118">Требования</span><span class="sxs-lookup"><span data-stu-id="19999-118">Requirements</span></span>



| <span data-ttu-id="19999-119">Требование</span><span class="sxs-lookup"><span data-stu-id="19999-119">Requirement</span></span> | <span data-ttu-id="19999-120">Значение</span><span class="sxs-lookup"><span data-stu-id="19999-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19999-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19999-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19999-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19999-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="19999-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19999-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19999-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19999-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19999-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="19999-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="19999-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19999-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19999-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19999-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="19999-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="19999-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19999-129">**релеасекаптуре**</span><span class="sxs-lookup"><span data-stu-id="19999-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="19999-130">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="19999-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="19999-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="19999-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="19999-132">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="19999-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

