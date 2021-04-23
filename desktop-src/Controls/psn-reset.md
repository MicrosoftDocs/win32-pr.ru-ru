---
title: Код уведомления PSN_RESET (Пршт. h)
description: Уведомляет страницу о том, что страница свойств собирается уничтожиться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654443"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="cda20-105">\_Код уведомления о сбросе PSN</span><span class="sxs-lookup"><span data-stu-id="cda20-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="cda20-106">Уведомляет страницу о том, что страница свойств собирается уничтожиться.</span><span class="sxs-lookup"><span data-stu-id="cda20-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="cda20-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cda20-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cda20-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cda20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda20-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cda20-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cda20-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="cda20-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda20-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cda20-111">Return value</span></span>

<span data-ttu-id="cda20-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="cda20-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda20-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cda20-113">Remarks</span></span>

<span data-ttu-id="cda20-114">Все изменения, внесенные с момента последнего PSN, отменяют код уведомления, за исключением случая, когда [**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), который не поддерживает этот код уведомления. [ \_](psn-apply.md)</span><span class="sxs-lookup"><span data-stu-id="cda20-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="cda20-115">Члену **lParam** структуры [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , на которую указывает *lParam* , будет присвоено значение **true** , если пользователь нащелкнул кнопку **X** в правом верхнем углу страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="cda20-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="cda20-116">**Значение false** , если пользователь нажмет кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="cda20-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="cda20-117">Структура **пшнотифи** содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="cda20-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="cda20-118">Приложение может использовать этот код уведомления как возможность выполнять операции очистки.</span><span class="sxs-lookup"><span data-stu-id="cda20-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="cda20-119">Страница свойств находится в процессе управления списком страниц при \_ отправке кода уведомления о сбросе PSN.</span><span class="sxs-lookup"><span data-stu-id="cda20-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="cda20-120">Не пытайтесь добавлять, удалять или вставлять страницы при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="cda20-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="cda20-121">Это приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="cda20-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="cda20-122">Не вызывайте функцию [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="cda20-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda20-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cda20-123">Requirements</span></span>



| <span data-ttu-id="cda20-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cda20-124">Requirement</span></span> | <span data-ttu-id="cda20-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cda20-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cda20-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cda20-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cda20-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cda20-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cda20-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cda20-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cda20-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cda20-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cda20-130">Header</span><span class="sxs-lookup"><span data-stu-id="cda20-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda20-131"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda20-131"><dt>Prsht.h</dt></span></span> </dl> |



 

