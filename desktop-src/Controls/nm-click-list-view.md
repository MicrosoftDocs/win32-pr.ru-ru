---
title: Код уведомления NM_CLICK (представление списка) (Коммктрл. h)
description: Посылается элементом управления "представление списка", когда пользователь щелкает элемент с левой кнопкой мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- Элементы управления Windows для кода уведомления NM_CLICK (представление списка)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d766767bfb742e5d7ea7c22a1266540a40d65b9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137878"
---
# <a name="nm_click-list-view-notification-code"></a><span data-ttu-id="a4852-105">\_Код уведомления Click (представление списка) NM</span><span class="sxs-lookup"><span data-stu-id="a4852-105">NM\_CLICK (list view) notification code</span></span>

<span data-ttu-id="a4852-106">Посылается элементом управления "представление списка", когда пользователь щелкает элемент с левой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="a4852-106">Sent by a list-view control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="a4852-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a4852-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a4852-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4852-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4852-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4852-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4852-110">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a4852-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="a4852-111">Указатель на структуру [**нмитемактивате**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="a4852-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="a4852-112">Члены этой структуры **Член iItem**, **iSubItem** и **птактион** содержат сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="a4852-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4852-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4852-113">Return value</span></span>

<span data-ttu-id="a4852-114">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="a4852-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4852-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4852-115">Remarks</span></span>

<span data-ttu-id="a4852-116">Элемент **Член iItem** объекта *lParam* допустим только в том случае, если была нажата метка значка или первого столбца.</span><span class="sxs-lookup"><span data-stu-id="a4852-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="a4852-117">Чтобы определить, какой элемент выбран при нажатии на другое место в строке, отправьте сообщение [**LVM \_ субитемхиттест**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="a4852-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4852-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a4852-118">Requirements</span></span>



| <span data-ttu-id="a4852-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a4852-119">Requirement</span></span> | <span data-ttu-id="a4852-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a4852-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4852-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4852-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4852-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4852-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4852-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4852-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4852-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4852-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4852-125">Header</span><span class="sxs-lookup"><span data-stu-id="a4852-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4852-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4852-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





