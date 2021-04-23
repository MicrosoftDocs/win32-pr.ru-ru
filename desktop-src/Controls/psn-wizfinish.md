---
title: Код уведомления PSN_WIZFINISH (Пршт. h)
description: Уведомляет страницу о нажатии пользователем кнопки Готово в мастере. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491784"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="36c26-105">\_Код уведомления PSN визфиниш</span><span class="sxs-lookup"><span data-stu-id="36c26-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="36c26-106">Уведомляет страницу о нажатии пользователем кнопки **Готово** в мастере.</span><span class="sxs-lookup"><span data-stu-id="36c26-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="36c26-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="36c26-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="36c26-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36c26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36c26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36c26-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="36c26-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="36c26-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="36c26-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="36c26-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="36c26-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c26-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36c26-113">Return value</span></span>

-   <span data-ttu-id="36c26-114">Возвращает **значение true** , чтобы не допустить завершения работы мастера.</span><span class="sxs-lookup"><span data-stu-id="36c26-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="36c26-115">Версия 5,80.</span><span class="sxs-lookup"><span data-stu-id="36c26-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="36c26-116">и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="36c26-116">and later.</span></span> <span data-ttu-id="36c26-117">Возвращает маркер окна для предотвращения завершения работы мастера.</span><span class="sxs-lookup"><span data-stu-id="36c26-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="36c26-118">Мастер настроит фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="36c26-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="36c26-119">Окно должно принадлежать странице мастера.</span><span class="sxs-lookup"><span data-stu-id="36c26-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="36c26-120">Возвращает **значение false** , чтобы разрешить завершение работы мастера.</span><span class="sxs-lookup"><span data-stu-id="36c26-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c26-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36c26-121">Remarks</span></span>

<span data-ttu-id="36c26-122">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с \_ значением мсгресулт DWL, а процедура диалогового окна должна возвращать значение **true**.</span><span class="sxs-lookup"><span data-stu-id="36c26-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="36c26-123">Версия 5,80.</span><span class="sxs-lookup"><span data-stu-id="36c26-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="36c26-124">Если приложение возвращает **значение true** для предотвращения завершения работы мастера, оно не управляет тем, какое окно на странице получает фокус.</span><span class="sxs-lookup"><span data-stu-id="36c26-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="36c26-125">Приложения, для которых требуется прекращение работы мастера, должны в обычном порядке вернуть маркер окна на странице мастера, которая должна получать фокус.</span><span class="sxs-lookup"><span data-stu-id="36c26-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c26-126">Требования</span><span class="sxs-lookup"><span data-stu-id="36c26-126">Requirements</span></span>



| <span data-ttu-id="36c26-127">Требование</span><span class="sxs-lookup"><span data-stu-id="36c26-127">Requirement</span></span> | <span data-ttu-id="36c26-128">Значение</span><span class="sxs-lookup"><span data-stu-id="36c26-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36c26-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36c26-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36c26-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36c26-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="36c26-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36c26-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36c26-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36c26-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36c26-133">Header</span><span class="sxs-lookup"><span data-stu-id="36c26-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c26-134"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c26-134"><dt>Prsht.h</dt></span></span> </dl> |



 

