---
title: Код уведомления PSN_QUERYINITIALFOCUS (Пршт. h)
description: Посылается на страницу свойств, чтобы предоставить странице страницы свойств возможность указать, какой элемент управления диалогового окна должен получать исходный фокус. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135207"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="937d8-105">\_Код уведомления PSN куеринитиалфокус</span><span class="sxs-lookup"><span data-stu-id="937d8-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="937d8-106">Посылается на страницу свойств, чтобы предоставить странице страницы свойств возможность указать, какой элемент управления диалогового окна должен получать исходный фокус.</span><span class="sxs-lookup"><span data-stu-id="937d8-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="937d8-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="937d8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="937d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="937d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="937d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="937d8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="937d8-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) .</span><span class="sxs-lookup"><span data-stu-id="937d8-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="937d8-111">Приведите член **lParam** этой структуры к типу **HWND** , чтобы получить дескриптор элемента управления, который по умолчанию будет получать фокус.</span><span class="sxs-lookup"><span data-stu-id="937d8-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="937d8-112">Структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="937d8-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="937d8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="937d8-113">Return value</span></span>

<span data-ttu-id="937d8-114">Чтобы указать, какой элемент управления должен получать фокус, возвратите маркер элемента управления.</span><span class="sxs-lookup"><span data-stu-id="937d8-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="937d8-115">В противном случае возвращается ноль и фокус перейдет к элементу управления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="937d8-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="937d8-116">Чтобы задать возвращаемое значение, процедура диалогового окна должна вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) со значением **DWL \_ Мсгресулт** и вернуть значение **true**.</span><span class="sxs-lookup"><span data-stu-id="937d8-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="937d8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="937d8-117">Remarks</span></span>

<span data-ttu-id="937d8-118">Приложение не должно вызывать функцию [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="937d8-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="937d8-119">Возвратить маркер элемента управления, который должен получать фокус, а диспетчер страниц свойств будет управлять изменением фокуса.</span><span class="sxs-lookup"><span data-stu-id="937d8-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="937d8-120">\_Код уведомления PSN куеринитиалфокус не отправляется, если диспетчер страниц свойств определяет, что ни один элемент управления на странице не должен получать фокус.</span><span class="sxs-lookup"><span data-stu-id="937d8-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="937d8-121">Этот фрагмент кода реализует простой обработчик для PSN \_ куеринитиалфокус.</span><span class="sxs-lookup"><span data-stu-id="937d8-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="937d8-122">Он запрашивает, что начальное фокус передается элементу управления Location (**\_ Расположение IDC**).</span><span class="sxs-lookup"><span data-stu-id="937d8-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="937d8-123">Этот код уведомления не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="937d8-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="937d8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="937d8-124">Requirements</span></span>



| <span data-ttu-id="937d8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="937d8-125">Requirement</span></span> | <span data-ttu-id="937d8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="937d8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="937d8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="937d8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="937d8-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="937d8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="937d8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="937d8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="937d8-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="937d8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="937d8-131">Header</span><span class="sxs-lookup"><span data-stu-id="937d8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="937d8-132"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="937d8-132"><dt>Prsht.h</dt></span></span> </dl> |



 

