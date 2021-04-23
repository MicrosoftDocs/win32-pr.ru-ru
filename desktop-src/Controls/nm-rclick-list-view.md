---
title: Код уведомления NM_RCLICK (представление списка) (Коммктрл. h)
description: Посылается элементом управления "представление списка", когда пользователь щелкает элемент правой кнопкой мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- Элементы управления Windows для кода уведомления NM_RCLICK (представление списка)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01c21f1b1e869a909dd41dcfce693bf084f2fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136055"
---
# <a name="nm_rclick-list-view-notification-code"></a><span data-ttu-id="80f61-105">\_Код уведомления NM ркликк (представление списка)</span><span class="sxs-lookup"><span data-stu-id="80f61-105">NM\_RCLICK (list view) notification code</span></span>

<span data-ttu-id="80f61-106">Посылается элементом управления "представление списка", когда пользователь щелкает элемент правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="80f61-106">Sent by a list-view control when the user clicks an item with the right mouse button.</span></span> <span data-ttu-id="80f61-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="80f61-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="80f61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80f61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80f61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80f61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80f61-110">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="80f61-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="80f61-111">Указатель на структуру [**нмитемактивате**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="80f61-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="80f61-112">Члены этой структуры **Член iItem**, **iSubItem** и **птактион** содержат сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="80f61-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80f61-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80f61-113">Return value</span></span>

<span data-ttu-id="80f61-114">Возвращает ненулевое значение, чтобы не разрешать обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80f61-114">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="80f61-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80f61-115">Remarks</span></span>

<span data-ttu-id="80f61-116">Элемент **Член iItem** объекта *lParam* допустим только в том случае, если была нажата метка значка или первого столбца.</span><span class="sxs-lookup"><span data-stu-id="80f61-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="80f61-117">Чтобы определить, какой элемент выбран при нажатии на другое место в строке, отправьте сообщение [**LVM \_ субитемхиттест**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="80f61-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f61-118">Требования</span><span class="sxs-lookup"><span data-stu-id="80f61-118">Requirements</span></span>



| <span data-ttu-id="80f61-119">Требование</span><span class="sxs-lookup"><span data-stu-id="80f61-119">Requirement</span></span> | <span data-ttu-id="80f61-120">Значение</span><span class="sxs-lookup"><span data-stu-id="80f61-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80f61-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80f61-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80f61-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80f61-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80f61-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80f61-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80f61-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80f61-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80f61-125">Header</span><span class="sxs-lookup"><span data-stu-id="80f61-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="80f61-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="80f61-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





