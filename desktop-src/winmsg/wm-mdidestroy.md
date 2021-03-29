---
description: Приложение отправляет \_ сообщение WM мдидестрой в окно клиента многодокументного интерфейса (MDI) для закрытия дочернего окна MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Сообщение WM_MDIDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809557"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="30efa-103">\_Сообщение МДИДЕСТРОЙ WM</span><span class="sxs-lookup"><span data-stu-id="30efa-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="30efa-104">Приложение отправляет сообщение **WM \_ мдидестрой** в окно клиента многодокументного интерфейса (MDI) для закрытия дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="30efa-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="30efa-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="30efa-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30efa-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30efa-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30efa-107">Маркер дочернего окна MDI, которое должно быть закрыто.</span><span class="sxs-lookup"><span data-stu-id="30efa-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="30efa-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30efa-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30efa-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="30efa-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30efa-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30efa-110">Return value</span></span>

<span data-ttu-id="30efa-111">Тип: **ноль**</span><span class="sxs-lookup"><span data-stu-id="30efa-111">Type: **zero**</span></span>

<span data-ttu-id="30efa-112">Это сообщение всегда возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="30efa-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="30efa-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30efa-113">Remarks</span></span>

<span data-ttu-id="30efa-114">Это сообщение удаляет заголовок дочернего окна MDI из окна фрейма MDI и деактивирует дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="30efa-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="30efa-115">Приложение должно использовать это сообщение, чтобы закрыть все дочерние окна MDI.</span><span class="sxs-lookup"><span data-stu-id="30efa-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="30efa-116">Если клиентское окно MDI получает сообщение, которое изменяет активацию дочерних окон, а активное дочернее окно MDI является развернутым, система восстанавливает активное дочернее окно и разворачивает вновь активированное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="30efa-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="30efa-117">Требования</span><span class="sxs-lookup"><span data-stu-id="30efa-117">Requirements</span></span>



| <span data-ttu-id="30efa-118">Требование</span><span class="sxs-lookup"><span data-stu-id="30efa-118">Requirement</span></span> | <span data-ttu-id="30efa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30efa-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30efa-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30efa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30efa-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30efa-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="30efa-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30efa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30efa-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30efa-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30efa-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="30efa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30efa-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30efa-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30efa-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30efa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="30efa-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="30efa-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30efa-128">**WM \_ мдикреате**</span><span class="sxs-lookup"><span data-stu-id="30efa-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="30efa-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="30efa-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30efa-130">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="30efa-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




