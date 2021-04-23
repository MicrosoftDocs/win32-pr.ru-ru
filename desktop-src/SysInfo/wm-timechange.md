---
description: Сообщение, которое отправляется при изменении системного времени.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: Сообщение WM_TIMECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662830"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="e8fe3-103">\_Сообщение ТИМЕЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="e8fe3-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="e8fe3-104">Сообщение, которое отправляется при изменении системного времени.</span><span class="sxs-lookup"><span data-stu-id="e8fe3-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="e8fe3-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e8fe3-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="e8fe3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8fe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fe3-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e8fe3-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e8fe3-108">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="e8fe3-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="e8fe3-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="e8fe3-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e8fe3-110">**WM \_ Идентификатор ТИМЕЧАНЖЕ** .</span><span class="sxs-lookup"><span data-stu-id="e8fe3-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8fe3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8fe3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8fe3-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e8fe3-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8fe3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8fe3-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8fe3-114">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e8fe3-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fe3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8fe3-115">Return value</span></span>

<span data-ttu-id="e8fe3-116">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e8fe3-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fe3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8fe3-117">Remarks</span></span>

<span data-ttu-id="e8fe3-118">Приложение не должно передавать это сообщение, так как система будет рассылать это сообщение, когда приложение изменяет системное время.</span><span class="sxs-lookup"><span data-stu-id="e8fe3-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8fe3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e8fe3-119">Requirements</span></span>



| <span data-ttu-id="e8fe3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e8fe3-120">Requirement</span></span> | <span data-ttu-id="e8fe3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e8fe3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fe3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8fe3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8fe3-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8fe3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e8fe3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8fe3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8fe3-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8fe3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8fe3-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8fe3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8fe3-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8fe3-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8fe3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8fe3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fe3-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="e8fe3-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

