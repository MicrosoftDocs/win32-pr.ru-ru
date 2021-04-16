---
description: Посылается в окно после того, как оно выйдет из модального цикла перемещения или изменения размера.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Сообщение WM_EXITSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719586"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="fe0e4-103">\_Сообщение ЕКСИТСИЗЕМОВЕ WM</span><span class="sxs-lookup"><span data-stu-id="fe0e4-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="fe0e4-104">Посылается в окно после того, как оно выйдет из модального цикла перемещения или изменения размера.</span><span class="sxs-lookup"><span data-stu-id="fe0e4-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="fe0e4-105">Окно перемещается в модальный цикл перемещения или изменения размера, когда пользователь щелкает заголовок окна или границу изменения размера, или когда окно передает сообщение [**WM \_ сискомманд**](../menurc/wm-syscommand.md) в функцию [**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , а параметр *wParam* сообщения указывает значение **SC \_ MOV** E или **SC \_ size** .</span><span class="sxs-lookup"><span data-stu-id="fe0e4-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="fe0e4-106">Операция завершается, когда [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает.</span><span class="sxs-lookup"><span data-stu-id="fe0e4-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="fe0e4-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe0e4-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="fe0e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe0e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe0e4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0e4-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fe0e4-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe0e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe0e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0e4-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fe0e4-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0e4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe0e4-113">Return value</span></span>

<span data-ttu-id="fe0e4-114">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="fe0e4-114">Type: **LRESULT**</span></span>

<span data-ttu-id="fe0e4-115">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="fe0e4-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0e4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fe0e4-116">Requirements</span></span>



| <span data-ttu-id="fe0e4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fe0e4-117">Requirement</span></span> | <span data-ttu-id="fe0e4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fe0e4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0e4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe0e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0e4-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe0e4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fe0e4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe0e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0e4-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe0e4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe0e4-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fe0e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0e4-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe0e4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0e4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe0e4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe0e4-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fe0e4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fe0e4-127">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="fe0e4-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="fe0e4-128">**WM \_ ентерсиземове**</span><span class="sxs-lookup"><span data-stu-id="fe0e4-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="fe0e4-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fe0e4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fe0e4-130">Windows</span><span class="sxs-lookup"><span data-stu-id="fe0e4-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
