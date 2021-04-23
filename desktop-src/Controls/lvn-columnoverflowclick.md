---
title: Код уведомления LVN_COLUMNOVERFLOWCLICK (Коммктрл. h)
description: Отправляется элементом управления "представление списка" при нажатии кнопки переполнения. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493335"
---
# <a name="lvn_columnoverflowclick-notification-code"></a><span data-ttu-id="01bbf-105">\_Код уведомления ЛВН колумноверфловкликк</span><span class="sxs-lookup"><span data-stu-id="01bbf-105">LVN\_COLUMNOVERFLOWCLICK notification code</span></span>

<span data-ttu-id="01bbf-106">Отправляется элементом управления "представление списка" при нажатии кнопки переполнения.</span><span class="sxs-lookup"><span data-stu-id="01bbf-106">Sent by a list-view control when its overflow button is clicked.</span></span> <span data-ttu-id="01bbf-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="01bbf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="01bbf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01bbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01bbf-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01bbf-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01bbf-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) , описывающую код уведомления.</span><span class="sxs-lookup"><span data-stu-id="01bbf-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="01bbf-111">Вызывающий объект отвечает за выделение этой структуры, включая вложенную структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="01bbf-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="01bbf-112">Задайте элементы структуры **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="01bbf-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="01bbf-113">Элемент **Code** должен иметь значение ЛВН \_ колумноверфловкликк.</span><span class="sxs-lookup"><span data-stu-id="01bbf-113">The **code** member must be set to LVN\_COLUMNOVERFLOWCLICK.</span></span>

<span data-ttu-id="01bbf-114">Задайте для элемента **Член iItem** структуры [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) значение-1.</span><span class="sxs-lookup"><span data-stu-id="01bbf-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="01bbf-115">Задайте для элемента **iSubItem** индекс подэлемента.</span><span class="sxs-lookup"><span data-stu-id="01bbf-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="01bbf-116">Задайте для членов **уневстате**, **уолдстате** и **lParam** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="01bbf-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="01bbf-117">Остальные элементы структуры **нмлиствиев** не используются.</span><span class="sxs-lookup"><span data-stu-id="01bbf-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01bbf-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01bbf-118">Return value</span></span>

<span data-ttu-id="01bbf-119">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="01bbf-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01bbf-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01bbf-120">Remarks</span></span>

<span data-ttu-id="01bbf-121">Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="01bbf-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="01bbf-122">Параметр *wParam* содержит идентификатор элемента управления, который отправляет код уведомления.</span><span class="sxs-lookup"><span data-stu-id="01bbf-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="01bbf-123">Если элемент управления "заголовок" является дочерним элементом ListView, элемент управления "заголовок" должен отправить этот код уведомления в элемент управления ListView, когда элемент управления "заголовок" получает код уведомления [ХДН \_ оверфловкликк](hdn-overflowclick.md) .</span><span class="sxs-lookup"><span data-stu-id="01bbf-123">If a header control is a child of the listview, the header control should send this notification code to the listview control when the header control receives the [HDN\_OVERFLOWCLICK](hdn-overflowclick.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01bbf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="01bbf-124">Requirements</span></span>



| <span data-ttu-id="01bbf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="01bbf-125">Requirement</span></span> | <span data-ttu-id="01bbf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="01bbf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01bbf-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01bbf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="01bbf-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01bbf-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01bbf-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01bbf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="01bbf-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01bbf-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01bbf-131">Header</span><span class="sxs-lookup"><span data-stu-id="01bbf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="01bbf-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="01bbf-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





