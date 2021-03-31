---
title: Код уведомления PSN_APPLY (Пршт. h)
description: Посылается на каждую страницу страницы свойств, чтобы указать, что пользователь щелкнул кнопку ОК, закрыть или применить и хочет, чтобы все изменения вступили в силу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491439"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="3948b-105">PSN \_ Применить код уведомления</span><span class="sxs-lookup"><span data-stu-id="3948b-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="3948b-106">Посылается на каждую страницу страницы свойств, чтобы указать, что пользователь щелкнул кнопку ОК, закрыть или применить и хочет, чтобы все изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="3948b-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="3948b-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3948b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3948b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3948b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3948b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3948b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3948b-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления, включая идентификатор страницы.</span><span class="sxs-lookup"><span data-stu-id="3948b-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3948b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3948b-111">Return value</span></span>

<span data-ttu-id="3948b-112">Установите ПСНРЕТ \_ -Error, чтобы указать, что изменения, внесенные на этой странице, являются допустимыми и применены.</span><span class="sxs-lookup"><span data-stu-id="3948b-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="3948b-113">Если все страницы задают ПСНРЕТ \_ , то страница свойств может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="3948b-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="3948b-114">Чтобы указать, что изменения, внесенные на этой странице, являются недопустимыми, и чтобы предотвратить уничтожение страницы свойств, установите одно из следующих возвращаемых значений:</span><span class="sxs-lookup"><span data-stu-id="3948b-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="3948b-115">ПСНРЕТ является \_ недопустимым.</span><span class="sxs-lookup"><span data-stu-id="3948b-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="3948b-116">Страница свойств не будет уничтожена, и на эту страницу будет возвращен фокус.</span><span class="sxs-lookup"><span data-stu-id="3948b-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="3948b-117">ПСНРЕТ \_ Недопустимый \_ ночанжепаже.</span><span class="sxs-lookup"><span data-stu-id="3948b-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="3948b-118">Страница свойств не будет уничтожена, и фокус будет возвращен на страницу, на которую находил фокус при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="3948b-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="3948b-119">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с \_ значением мсгресулт DWL, а процедура диалогового окна должна возвращать значение **true**.</span><span class="sxs-lookup"><span data-stu-id="3948b-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3948b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3948b-120">Remarks</span></span>

<span data-ttu-id="3948b-121">Когда пользователь нажимает кнопку ОК, применить или закрыть, страница свойств отправляет на активную страницу уведомление [PSN \_ киллактиве](psn-killactive.md) , давая ему возможность проверить изменения, внесенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="3948b-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="3948b-122">Если изменения допустимы, страница свойств отправляет PSN \_ Применить код уведомления на каждую страницу, направляя его для применения новых свойств к соответствующему элементу.</span><span class="sxs-lookup"><span data-stu-id="3948b-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="3948b-123">Страница свойств находится в процессе управления списком страниц при \_ отправке кода уведомления о применении PSN.</span><span class="sxs-lookup"><span data-stu-id="3948b-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="3948b-124">Не пытайтесь добавлять, удалять или вставлять страницы при обработке этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="3948b-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="3948b-125">Это приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="3948b-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="3948b-126">Члену **lParam** структуры [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , на которую указывает *lParam* , присваивается **значение true** , если пользователь нажимает кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="3948b-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="3948b-127">Также устанавливается значение **true** , если сообщение [**ПСМ \_ канцелтоклосе**](psm-canceltoclose.md) было отправлено и пользователь нажимает кнопку Закрыть.</span><span class="sxs-lookup"><span data-stu-id="3948b-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="3948b-128">Если пользователь нажмет кнопку "Применить", он имеет значение **false** .</span><span class="sxs-lookup"><span data-stu-id="3948b-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="3948b-129">Структура [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="3948b-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="3948b-130">Не вызывайте функцию [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="3948b-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="3948b-131">Модальная страница свойств уничтожается, если пользователь нажимает кнопку ОК, и каждая страница возвращает \_ значение пснрет в ответ на **PSN \_ Apply**.</span><span class="sxs-lookup"><span data-stu-id="3948b-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="3948b-132">Если какая-либо страница возвращает ПСНРЕТ \_ недопустимую или пснрет \_ недопустимую \_ Ночанжепаже, процесс применения немедленно отменяется.</span><span class="sxs-lookup"><span data-stu-id="3948b-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="3948b-133">Страницы после отмены страницы не получат PSN \_ код уведомления.</span><span class="sxs-lookup"><span data-stu-id="3948b-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="3948b-134">Чтобы получить этот код уведомления, на странице необходимо задать для параметра DWL \_ мсгресулт значение **false** в ответ на код [уведомления \_ киллактиве PSN](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="3948b-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="3948b-135">Этот код уведомления не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="3948b-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3948b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3948b-136">Requirements</span></span>



| <span data-ttu-id="3948b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3948b-137">Requirement</span></span> | <span data-ttu-id="3948b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3948b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3948b-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3948b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3948b-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3948b-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3948b-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3948b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3948b-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3948b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3948b-143">Header</span><span class="sxs-lookup"><span data-stu-id="3948b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3948b-144"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="3948b-144"><dt>Prsht.h</dt></span></span> </dl> |



 

