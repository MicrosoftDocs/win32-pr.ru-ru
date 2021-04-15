---
title: Код уведомления PSN_TRANSLATEACCELERATOR (Пршт. h)
description: Уведомляет вкладку свойств о получении сообщения клавиатуры. Она предоставляет странице возможность сделать закрытый клавиатурный перевод с помощью сочетания клавиш. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654423"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="2e69b-106">\_Код уведомления PSN TRANSLATEACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="2e69b-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="2e69b-107">Уведомляет вкладку свойств о получении сообщения клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="2e69b-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="2e69b-108">Она предоставляет странице возможность сделать закрытый клавиатурный перевод с помощью сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="2e69b-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="2e69b-109">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2e69b-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2e69b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e69b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e69b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e69b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e69b-112">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="2e69b-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="2e69b-113">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="2e69b-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="2e69b-114">Член **lParam** структуры **пшнотифи** — это указатель [**на сообщение сообщения.**](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="2e69b-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="2e69b-115">Его можно привести к типу **лпмсг** , чтобы получить доступ к параметрам сообщения, которое необходимо перевести.</span><span class="sxs-lookup"><span data-stu-id="2e69b-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e69b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e69b-116">Return value</span></span>

<span data-ttu-id="2e69b-117">Возвращает ПСНРЕТ \_ мессажехандлед, чтобы указать, что дальнейшая обработка не требуется.</span><span class="sxs-lookup"><span data-stu-id="2e69b-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="2e69b-118">Возвращает ПСНРЕТ \_ , чтобы запросить нормальную обработку.</span><span class="sxs-lookup"><span data-stu-id="2e69b-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e69b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e69b-119">Remarks</span></span>

<span data-ttu-id="2e69b-120">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) со \_ значением DWL мсгресулт.</span><span class="sxs-lookup"><span data-stu-id="2e69b-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="2e69b-121">Процедура диалогового окна должна возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="2e69b-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e69b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2e69b-122">Requirements</span></span>



| <span data-ttu-id="2e69b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2e69b-123">Requirement</span></span> | <span data-ttu-id="2e69b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2e69b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e69b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e69b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e69b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e69b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e69b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e69b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e69b-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e69b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e69b-129">Header</span><span class="sxs-lookup"><span data-stu-id="2e69b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e69b-130"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e69b-130"><dt>Prsht.h</dt></span></span> </dl> |



 

