---
description: Посылается, когда будет активировано окно, принадлежащее другому приложению, чем активное окно. Сообщение отправляется в приложение, окно которого активируется, и в приложение, окно которого деактивируется.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Сообщение WM_ACTIVATEAPP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702585"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="3b1d0-104">\_Сообщение АКТИВАТЕАПП WM</span><span class="sxs-lookup"><span data-stu-id="3b1d0-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="3b1d0-105">Посылается, когда будет активировано окно, принадлежащее другому приложению, чем активное окно.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="3b1d0-106">Сообщение отправляется в приложение, окно которого активируется, и в приложение, окно которого деактивируется.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="3b1d0-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b1d0-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="3b1d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b1d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b1d0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b1d0-110">Указывает, активируется ли окно или деактивируется.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="3b1d0-111">Этот параметр имеет **значение true** , если окно активируется; **значение false** , если окно деактивируется.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="3b1d0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b1d0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b1d0-113">Идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-113">The thread identifier.</span></span> <span data-ttu-id="3b1d0-114">Если параметр *wParam* имеет **значение true**, то аргумент *lParam* является идентификатором потока, владеющего активным окном.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="3b1d0-115">Если параметр *wParam* имеет **значение false**, то параметр *lParam* является идентификатором потока, владеющего активным окном.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1d0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b1d0-116">Return value</span></span>

<span data-ttu-id="3b1d0-117">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="3b1d0-117">Type: **LRESULT**</span></span>

<span data-ttu-id="3b1d0-118">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3b1d0-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b1d0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3b1d0-119">Requirements</span></span>



| <span data-ttu-id="3b1d0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3b1d0-120">Requirement</span></span> | <span data-ttu-id="3b1d0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3b1d0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1d0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b1d0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b1d0-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b1d0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3b1d0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b1d0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b1d0-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b1d0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b1d0-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b1d0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b1d0-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b1d0-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b1d0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b1d0-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b1d0-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3b1d0-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b1d0-130">**\_Активация WM**</span><span class="sxs-lookup"><span data-stu-id="3b1d0-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="3b1d0-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3b1d0-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3b1d0-132">Windows</span><span class="sxs-lookup"><span data-stu-id="3b1d0-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
