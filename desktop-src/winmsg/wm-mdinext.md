---
description: Приложение отправляет \_ сообщение WM мдинекст в окно клиента многодокументного интерфейса (MDI) для активации следующего или предыдущего дочернего окна.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Сообщение WM_MDINEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809556"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="e79f8-103">\_Сообщение МДИНЕКСТ WM</span><span class="sxs-lookup"><span data-stu-id="e79f8-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="e79f8-104">Приложение отправляет сообщение **WM \_ мдинекст** в окно клиента многодокументного интерфейса (MDI) для активации следующего или предыдущего дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="e79f8-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="e79f8-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e79f8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e79f8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e79f8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e79f8-107">Маркер дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="e79f8-107">A handle to the MDI child window.</span></span> <span data-ttu-id="e79f8-108">Система активирует дочернее окно, которое непосредственно перед указанным дочерним окном или после него, в зависимости от значения параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e79f8-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="e79f8-109">Если параметр *wParam* имеет **значение NULL**, система активирует дочернее окно, которое непосредственно до или после активного текущего дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="e79f8-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="e79f8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e79f8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e79f8-111">Если этот параметр равен нулю, система активирует следующее дочернее окно MDI и помещает дочернее окно, определяемое параметром *wParam* , за всеми остальными дочерними окнами.</span><span class="sxs-lookup"><span data-stu-id="e79f8-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="e79f8-112">Если этот параметр не равен нулю, система активирует предыдущее дочернее окно, помещая его перед дочерним окном, идентифицируемым *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e79f8-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e79f8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e79f8-113">Return value</span></span>

<span data-ttu-id="e79f8-114">Тип: **ноль**</span><span class="sxs-lookup"><span data-stu-id="e79f8-114">Type: **zero**</span></span>

<span data-ttu-id="e79f8-115">Возвращаемое значение всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e79f8-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e79f8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e79f8-116">Remarks</span></span>

<span data-ttu-id="e79f8-117">Если клиентское MDI-окно получает сообщение, которое изменяет активацию своих дочерних окон, когда активное дочернее окно MDI развернуто, система восстанавливает активное дочернее окно и разворачивает вновь активированное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="e79f8-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e79f8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e79f8-118">Requirements</span></span>



| <span data-ttu-id="e79f8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e79f8-119">Requirement</span></span> | <span data-ttu-id="e79f8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e79f8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e79f8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e79f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e79f8-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e79f8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e79f8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e79f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e79f8-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e79f8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e79f8-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e79f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e79f8-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e79f8-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e79f8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e79f8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e79f8-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e79f8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e79f8-129">**WM \_ мдиактивате**</span><span class="sxs-lookup"><span data-stu-id="e79f8-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="e79f8-130">**WM \_ мдижетактиве**</span><span class="sxs-lookup"><span data-stu-id="e79f8-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="e79f8-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e79f8-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e79f8-132">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="e79f8-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




