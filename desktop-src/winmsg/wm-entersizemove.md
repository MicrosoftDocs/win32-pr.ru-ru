---
description: Посылается окну после того, как оно попадает в модальный цикл перемещения или изменения размера.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Сообщение WM_ENTERSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702577"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="597f0-103">\_Сообщение ЕНТЕРСИЗЕМОВЕ WM</span><span class="sxs-lookup"><span data-stu-id="597f0-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="597f0-104">Посылается окну после того, как оно попадает в модальный цикл перемещения или изменения размера.</span><span class="sxs-lookup"><span data-stu-id="597f0-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="597f0-105">Окно перемещается в модальный цикл перемещения или изменения размера, когда пользователь щелкает заголовок окна или границу изменения размера, или когда окно передает сообщение [**WM \_ сискомманд**](../menurc/wm-syscommand.md) в функцию [**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , а параметр *wParam* сообщения указывает значение **SC \_ Move** или **SC \_ size** .</span><span class="sxs-lookup"><span data-stu-id="597f0-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="597f0-106">Операция завершается, когда [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает.</span><span class="sxs-lookup"><span data-stu-id="597f0-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="597f0-107">Система отправляет сообщение **WM \_ ентерсиземове** независимо от того, включено ли перетаскивание всех окон.</span><span class="sxs-lookup"><span data-stu-id="597f0-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="597f0-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="597f0-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="597f0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="597f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="597f0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="597f0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="597f0-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="597f0-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="597f0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="597f0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="597f0-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="597f0-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="597f0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="597f0-114">Return value</span></span>

<span data-ttu-id="597f0-115">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="597f0-115">Type: **LRESULT**</span></span>

<span data-ttu-id="597f0-116">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="597f0-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="597f0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="597f0-117">Requirements</span></span>



| <span data-ttu-id="597f0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="597f0-118">Requirement</span></span> | <span data-ttu-id="597f0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="597f0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="597f0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="597f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="597f0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="597f0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="597f0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="597f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="597f0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="597f0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="597f0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="597f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="597f0-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="597f0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="597f0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="597f0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="597f0-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="597f0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="597f0-128">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="597f0-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="597f0-129">**WM \_ екситсиземове**</span><span class="sxs-lookup"><span data-stu-id="597f0-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="597f0-130">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="597f0-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="597f0-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="597f0-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="597f0-132">Windows</span><span class="sxs-lookup"><span data-stu-id="597f0-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
