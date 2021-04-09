---
description: Отправляется на значок, когда пользователь запрашивает восстановление окна до его предыдущего размера и расположения.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Сообщение WM_QUERYOPEN (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080807"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="431df-103">\_Сообщение КУЕРЙОПЕН WM</span><span class="sxs-lookup"><span data-stu-id="431df-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="431df-104">Отправляется на значок, когда пользователь запрашивает восстановление окна до его предыдущего размера и расположения.</span><span class="sxs-lookup"><span data-stu-id="431df-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="431df-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="431df-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="431df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="431df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="431df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="431df-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="431df-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="431df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="431df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="431df-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="431df-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431df-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="431df-111">Return value</span></span>

<span data-ttu-id="431df-112">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="431df-112">Type: **LRESULT**</span></span>

<span data-ttu-id="431df-113">Если значок можно открыть, приложение, обрабатывающее это сообщение, должно возвращать **значение true**; в противном случае возвращается **значение false** , чтобы предотвратить открытие значка.</span><span class="sxs-lookup"><span data-stu-id="431df-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="431df-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="431df-114">Remarks</span></span>

<span data-ttu-id="431df-115">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="431df-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="431df-116">При обработке этого сообщения приложение не должно выполнять никаких действий, вызывающих изменение активации или фокуса (например, создание диалогового окна).</span><span class="sxs-lookup"><span data-stu-id="431df-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="431df-117">Требования</span><span class="sxs-lookup"><span data-stu-id="431df-117">Requirements</span></span>



| <span data-ttu-id="431df-118">Требование</span><span class="sxs-lookup"><span data-stu-id="431df-118">Requirement</span></span> | <span data-ttu-id="431df-119">Значение</span><span class="sxs-lookup"><span data-stu-id="431df-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431df-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="431df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="431df-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="431df-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="431df-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="431df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="431df-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="431df-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="431df-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="431df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="431df-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="431df-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431df-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="431df-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="431df-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="431df-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="431df-128">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="431df-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="431df-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="431df-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="431df-130">Windows</span><span class="sxs-lookup"><span data-stu-id="431df-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
