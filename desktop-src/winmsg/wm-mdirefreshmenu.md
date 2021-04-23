---
description: Приложение отправляет \_ сообщение WM мдирефрешмену в окно клиента многодокументного интерфейса (MDI) для обновления меню окна фрейма окна MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Сообщение WM_MDIREFRESHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673825"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="4b6d2-103">\_Сообщение МДИРЕФРЕШМЕНУ WM</span><span class="sxs-lookup"><span data-stu-id="4b6d2-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="4b6d2-104">Приложение отправляет сообщение **WM \_ мдирефрешмену** в окно клиента многодокументного интерфейса (MDI) для обновления меню окна фрейма окна MDI.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="4b6d2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b6d2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b6d2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b6d2-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6d2-107">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4b6d2-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b6d2-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6d2-109">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b6d2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b6d2-110">Return value</span></span>

<span data-ttu-id="4b6d2-111">Тип: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="4b6d2-111">Type: **HMENU**</span></span>

<span data-ttu-id="4b6d2-112">Если сообщение прошло удачно, возвращаемое значение является маркером меню окна фрейма.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="4b6d2-113">Если сообщение не выполняется, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b6d2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b6d2-114">Remarks</span></span>

<span data-ttu-id="4b6d2-115">После отправки этого сообщения приложение должно вызвать функцию [**дравменубар**](/windows/win32/api/winuser/nf-winuser-drawmenubar) для обновления строки меню.</span><span class="sxs-lookup"><span data-stu-id="4b6d2-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6d2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4b6d2-116">Requirements</span></span>



| <span data-ttu-id="4b6d2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4b6d2-117">Requirement</span></span> | <span data-ttu-id="4b6d2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6d2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6d2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b6d2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4b6d2-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b6d2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4b6d2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b6d2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4b6d2-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b6d2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b6d2-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b6d2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b6d2-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b6d2-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b6d2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b6d2-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b6d2-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4b6d2-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b6d2-127">**дравменубар**</span><span class="sxs-lookup"><span data-stu-id="4b6d2-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="4b6d2-128">**WM \_ мдисетмену**</span><span class="sxs-lookup"><span data-stu-id="4b6d2-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="4b6d2-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="4b6d2-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b6d2-130">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="4b6d2-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
