---
description: Посылается всем окнам после входа или отключения пользователем. Когда пользователь входит в систему или выключается, система обновляет пользовательские параметры. Система отправляет это сообщение сразу после обновления параметров.
title: Сообщение WM_USERCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999416"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="dc3d1-105">\_Сообщение УСЕРЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="dc3d1-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="dc3d1-106">Посылается всем окнам после входа или отключения пользователем.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="dc3d1-107">Когда пользователь входит в систему или выключается, система обновляет пользовательские параметры.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="dc3d1-108">Система отправляет это сообщение сразу после обновления параметров.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="dc3d1-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc3d1-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="dc3d1-110">Это сообщение не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="dc3d1-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc3d1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc3d1-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc3d1-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc3d1-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc3d1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc3d1-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc3d1-115">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc3d1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc3d1-116">Return value</span></span>

<span data-ttu-id="dc3d1-117">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="dc3d1-117">Type: **LRESULT**</span></span>

<span data-ttu-id="dc3d1-118">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="dc3d1-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc3d1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="dc3d1-119">Requirements</span></span>



| <span data-ttu-id="dc3d1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="dc3d1-120">Requirement</span></span> | <span data-ttu-id="dc3d1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dc3d1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc3d1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc3d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc3d1-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dc3d1-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc3d1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc3d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc3d1-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dc3d1-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="dc3d1-126">Header</span><span class="sxs-lookup"><span data-stu-id="dc3d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc3d1-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc3d1-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc3d1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc3d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc3d1-129">Обзор Windows</span><span class="sxs-lookup"><span data-stu-id="dc3d1-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
