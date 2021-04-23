---
title: Код уведомления LVN_ITEMCHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент изменился. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654732"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="73b6e-105">\_Код уведомления ЛВН итемчанжед</span><span class="sxs-lookup"><span data-stu-id="73b6e-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="73b6e-106">Сообщает родительскому окну элемента управления "представление списка", что элемент изменился.</span><span class="sxs-lookup"><span data-stu-id="73b6e-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="73b6e-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73b6e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="73b6e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="73b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73b6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73b6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73b6e-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) , которая идентифицирует элемент и указывает, какие из его атрибутов изменились.</span><span class="sxs-lookup"><span data-stu-id="73b6e-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="73b6e-111">Если элемент **Член iItem** структуры, на который указывает *lParam* , имеет значение-1, это изменение было применено ко всем элементам в представлении списка.</span><span class="sxs-lookup"><span data-stu-id="73b6e-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73b6e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73b6e-112">Return value</span></span>

<span data-ttu-id="73b6e-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="73b6e-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73b6e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73b6e-114">Remarks</span></span>

<span data-ttu-id="73b6e-115">Если элемент управления "список" имеет стиль [**LVS \_ овнердата**](list-view-window-styles.md) , и пользователь выбирает диапазон элементов, удерживая клавишу Shift и щелкая мышью, \_ коды уведомлений ЛВН итемчанжед не отправляются для каждого выбранного или снятого элемента.</span><span class="sxs-lookup"><span data-stu-id="73b6e-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="73b6e-116">Вместо этого вы получите один код уведомления [ЛВН \_ одстатечанжед](lvn-odstatechanged.md) , указывающий, что диапазон элементов изменил состояние.</span><span class="sxs-lookup"><span data-stu-id="73b6e-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b6e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="73b6e-117">Requirements</span></span>



| <span data-ttu-id="73b6e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="73b6e-118">Requirement</span></span> | <span data-ttu-id="73b6e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="73b6e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73b6e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73b6e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73b6e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73b6e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73b6e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73b6e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73b6e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73b6e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73b6e-124">Header</span><span class="sxs-lookup"><span data-stu-id="73b6e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73b6e-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="73b6e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





