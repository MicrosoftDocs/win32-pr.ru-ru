---
title: Сообщение WM_CHANGECBCHAIN (Winuser. h)
description: Отправляется в первое окно в цепочке окна просмотра буфера обмена при удалении окна из цепочки. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Обмен данными с сообщениями WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136171"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="9625b-105">\_Сообщение ЧАНЖЕКБЧАИН WM</span><span class="sxs-lookup"><span data-stu-id="9625b-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="9625b-106">Отправляется в первое окно в цепочке окна просмотра буфера обмена при удалении окна из цепочки.</span><span class="sxs-lookup"><span data-stu-id="9625b-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="9625b-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9625b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="9625b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9625b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9625b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9625b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9625b-110">Маркер окна, удаляемого из цепочки средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="9625b-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="9625b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9625b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9625b-112">Маркер следующего окна в цепочке после удаляемого окна.</span><span class="sxs-lookup"><span data-stu-id="9625b-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="9625b-113">Этот параметр имеет **значение NULL** , если удаляемое окно является последним окном в цепочке.</span><span class="sxs-lookup"><span data-stu-id="9625b-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9625b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9625b-114">Return value</span></span>

<span data-ttu-id="9625b-115">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="9625b-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9625b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9625b-116">Remarks</span></span>

<span data-ttu-id="9625b-117">Каждое окно просмотра буфера обмена сохраняет маркер в следующем окне в цепочке окна просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="9625b-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="9625b-118">Изначально этот маркер является возвращаемым значением функции [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="9625b-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="9625b-119">Когда окно просмотра буфера обмена получает сообщение **WM \_ чанжекбчаин** , оно должно вызывать функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) для передачи сообщения следующему окну в цепочке, если только следующее окно не является удаляемым окном.</span><span class="sxs-lookup"><span data-stu-id="9625b-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="9625b-120">В этом случае средство просмотра буфера обмена должно сохранить маркер, заданный параметром *lParam* , в качестве следующего окна в цепочке.</span><span class="sxs-lookup"><span data-stu-id="9625b-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="9625b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9625b-121">Requirements</span></span>



| <span data-ttu-id="9625b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9625b-122">Requirement</span></span> | <span data-ttu-id="9625b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9625b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9625b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9625b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9625b-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9625b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9625b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9625b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9625b-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9625b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9625b-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9625b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9625b-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9625b-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9625b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9625b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="9625b-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9625b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9625b-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="9625b-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="9625b-133">**сетклипбоардвиевер**</span><span class="sxs-lookup"><span data-stu-id="9625b-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="9625b-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9625b-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9625b-135">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="9625b-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

