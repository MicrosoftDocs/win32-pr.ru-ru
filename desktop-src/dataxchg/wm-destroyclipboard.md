---
title: Сообщение WM_DESTROYCLIPBOARD (Winuser. h)
description: Отправляется владельцу буфера обмена, когда вызов функции Емптиклипбоард очищает буфер обмена. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- Обмен данными с сообщениями WM_DESTROYCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989384"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="83c44-105">\_Сообщение ДЕСТРОЙКЛИПБОАРД WM</span><span class="sxs-lookup"><span data-stu-id="83c44-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="83c44-106">Отправляется владельцу буфера обмена, когда вызов функции [**емптиклипбоард**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) очищает буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="83c44-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="83c44-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="83c44-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="83c44-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83c44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c44-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83c44-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83c44-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="83c44-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="83c44-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83c44-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83c44-112">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="83c44-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c44-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83c44-113">Return value</span></span>

<span data-ttu-id="83c44-114">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="83c44-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c44-115">Требования</span><span class="sxs-lookup"><span data-stu-id="83c44-115">Requirements</span></span>



| <span data-ttu-id="83c44-116">Требование</span><span class="sxs-lookup"><span data-stu-id="83c44-116">Requirement</span></span> | <span data-ttu-id="83c44-117">Значение</span><span class="sxs-lookup"><span data-stu-id="83c44-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c44-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83c44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83c44-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83c44-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="83c44-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83c44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83c44-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83c44-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83c44-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="83c44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c44-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83c44-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c44-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83c44-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="83c44-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="83c44-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83c44-126">**емптиклипбоард**</span><span class="sxs-lookup"><span data-stu-id="83c44-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="83c44-127">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="83c44-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="83c44-128">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="83c44-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

