---
title: Код уведомления PSN_QUERYCANCEL (Пршт. h)
description: Указывает, что пользователь отменил вкладку свойств. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988546"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="6e0fd-105">\_Код уведомления PSN QueryCancel с начала</span><span class="sxs-lookup"><span data-stu-id="6e0fd-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="6e0fd-106">Указывает, что пользователь отменил вкладку свойств.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="6e0fd-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0fd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="6e0fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e0fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e0fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e0fd-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="6e0fd-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="6e0fd-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0fd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e0fd-113">Return value</span></span>

<span data-ttu-id="6e0fd-114">Возвращает **значение true** , чтобы предотвратить операцию отмены, или **false** , чтобы разрешить ее.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0fd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e0fd-115">Remarks</span></span>

<span data-ttu-id="6e0fd-116">Этот код уведомления обычно отправляется, когда пользователь нажимает кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="6e0fd-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="6e0fd-117">Он также отправляется, когда пользователь нажимает кнопку **X** в правом верхнем углу страницы свойств или нажимает клавишу Escape.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="6e0fd-118">Страница страницы свойств может справиться с этим кодом уведомления, чтобы попросить пользователя проверить операцию отмены.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="6e0fd-119">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с параметром DWL \_ мсгресулт, для которого задано возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="6e0fd-120">Процедура диалогового окна должна возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0fd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6e0fd-121">Requirements</span></span>



| <span data-ttu-id="6e0fd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6e0fd-122">Requirement</span></span> | <span data-ttu-id="6e0fd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6e0fd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0fd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e0fd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0fd-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e0fd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6e0fd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e0fd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0fd-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e0fd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6e0fd-128">Header</span><span class="sxs-lookup"><span data-stu-id="6e0fd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0fd-129"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0fd-129"><dt>Prsht.h</dt></span></span> </dl> |



 

