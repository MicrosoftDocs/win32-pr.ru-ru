---
description: Приложение отправляет \_ сообщение WM мдиактивате в клиентский окно интерфейса MDI, чтобы указать клиентскому окну активировать другое дочернее окно MDI.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Сообщение WM_MDIACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647367"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="b31d2-103">\_Сообщение МДИАКТИВАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="b31d2-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="b31d2-104">Приложение отправляет сообщение **WM \_ мдиактивате** в клиентский окно интерфейса MDI, чтобы указать клиентскому окну активировать другое дочернее окно MDI.</span><span class="sxs-lookup"><span data-stu-id="b31d2-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="b31d2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b31d2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b31d2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b31d2-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b31d2-107">Маркер дочернего окна MDI, которое должно быть активировано.</span><span class="sxs-lookup"><span data-stu-id="b31d2-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="b31d2-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b31d2-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b31d2-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b31d2-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b31d2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b31d2-110">Return value</span></span>

<span data-ttu-id="b31d2-111">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="b31d2-111">Type: **LRESULT**</span></span>

<span data-ttu-id="b31d2-112">Если приложение отправляет это сообщение в окно клиента MDI, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b31d2-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="b31d2-113">Дочернее окно MDI должно вернуть нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="b31d2-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b31d2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b31d2-114">Remarks</span></span>

<span data-ttu-id="b31d2-115">Когда клиентское окно обрабатывает это сообщение, оно отправляет **WM \_ мдиактивате** в дочернее окно, которое деактивируется, а также активируется дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="b31d2-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="b31d2-116">Ниже приведены параметры сообщений, получаемые дочерним окном MDI.</span><span class="sxs-lookup"><span data-stu-id="b31d2-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="b31d2-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b31d2-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b31d2-118">Маркер дочернего окна MDI, деактивируемого.</span><span class="sxs-lookup"><span data-stu-id="b31d2-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="b31d2-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b31d2-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b31d2-120">Активируется маркер дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="b31d2-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="b31d2-121">Дочернее окно MDI активируется независимо от окна фрейма MDI.</span><span class="sxs-lookup"><span data-stu-id="b31d2-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="b31d2-122">Когда окно фрейма станет активным, дочернее окно, которое было в последний раз активировано с помощью сообщения **WM \_ мдиактивате** , получает сообщение [**WM \_ нкактивате**](wm-ncactivate.md) , которое Рисует рамку активного окна и строку заголовка; дочернее окно не получает другое сообщение **WM \_ мдиактивате** .</span><span class="sxs-lookup"><span data-stu-id="b31d2-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b31d2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b31d2-123">Requirements</span></span>



| <span data-ttu-id="b31d2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b31d2-124">Requirement</span></span> | <span data-ttu-id="b31d2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b31d2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b31d2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b31d2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b31d2-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b31d2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b31d2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b31d2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b31d2-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b31d2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b31d2-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b31d2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b31d2-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b31d2-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b31d2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b31d2-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="b31d2-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b31d2-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b31d2-134">**WM \_ мдижетактиве**</span><span class="sxs-lookup"><span data-stu-id="b31d2-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="b31d2-135">**WM \_ мдинекст**</span><span class="sxs-lookup"><span data-stu-id="b31d2-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="b31d2-136">**WM \_ нкактивате**</span><span class="sxs-lookup"><span data-stu-id="b31d2-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="b31d2-137">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b31d2-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b31d2-138">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="b31d2-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




