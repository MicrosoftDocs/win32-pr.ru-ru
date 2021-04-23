---
title: Код уведомления LVN_COLUMNDROPDOWN (Коммктрл. h)
description: Отправляется элементом управления "представление списка" при нажатии кнопки раскрывающегося списка представления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- LVN_COLUMNDROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534175"
---
# <a name="lvn_columndropdown-notification-code"></a><span data-ttu-id="2e87a-105">\_Код уведомления ЛВН колумндропдовн</span><span class="sxs-lookup"><span data-stu-id="2e87a-105">LVN\_COLUMNDROPDOWN notification code</span></span>

<span data-ttu-id="2e87a-106">Отправляется элементом управления "представление списка" при нажатии кнопки раскрывающегося списка представления.</span><span class="sxs-lookup"><span data-stu-id="2e87a-106">Sent by a list-view control when the list-view's drop-down button is pressed.</span></span> <span data-ttu-id="2e87a-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2e87a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2e87a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e87a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e87a-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e87a-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) , описывающую код уведомления.</span><span class="sxs-lookup"><span data-stu-id="2e87a-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="2e87a-111">Вызывающий объект отвечает за выделение этой структуры, включая вложенную структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="2e87a-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="2e87a-112">Задайте элементы структуры **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="2e87a-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="2e87a-113">Элемент **Code** должен иметь значение ЛВН \_ колумндропдовн.</span><span class="sxs-lookup"><span data-stu-id="2e87a-113">The **code** member must be set to LVN\_COLUMNDROPDOWN.</span></span>

<span data-ttu-id="2e87a-114">Задайте для элемента **Член iItem** структуры [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) значение-1.</span><span class="sxs-lookup"><span data-stu-id="2e87a-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="2e87a-115">Задайте для элемента **iSubItem** индекс подэлемента.</span><span class="sxs-lookup"><span data-stu-id="2e87a-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="2e87a-116">Задайте для членов **уневстате**, **уолдстате** и **lParam** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2e87a-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="2e87a-117">Остальные элементы структуры **нмлиствиев** не используются.</span><span class="sxs-lookup"><span data-stu-id="2e87a-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e87a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e87a-118">Return value</span></span>

<span data-ttu-id="2e87a-119">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2e87a-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e87a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e87a-120">Remarks</span></span>

<span data-ttu-id="2e87a-121">Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="2e87a-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="2e87a-122">Параметр *wParam* содержит идентификатор элемента управления, который отправляет код уведомления.</span><span class="sxs-lookup"><span data-stu-id="2e87a-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="2e87a-123">Если элемент управления "заголовок" является дочерним по отношению к представлению списка, элемент управления "заголовок" должен отправить этот код уведомлений в элемент управления "представление списка", когда элемент управления "заголовок" получит код уведомления [ \_ раскрывающегося списка ХДН](hdn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="2e87a-123">If a header control is a child of the list-view, the header control should send this notidication code to the list-view control when the header control receives the [HDN\_DROPDOWN](hdn-dropdown.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e87a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2e87a-124">Requirements</span></span>



| <span data-ttu-id="2e87a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2e87a-125">Requirement</span></span> | <span data-ttu-id="2e87a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2e87a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e87a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e87a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e87a-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e87a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e87a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e87a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e87a-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e87a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e87a-131">Header</span><span class="sxs-lookup"><span data-stu-id="2e87a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e87a-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e87a-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





