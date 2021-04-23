---
title: Код уведомления NM_RDBLCLK (представление списка) (Коммктрл. h)
description: Посылается элементом управления "представление списка", когда пользователь дважды щелкает элемент с правой кнопкой мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- Элементы управления Windows для кода уведомления NM_RDBLCLK (представление списка)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989443"
---
# <a name="nm_rdblclk-list-view-notification-code"></a><span data-ttu-id="e8c03-105">\_Код уведомления NM рдблклк (представление списка)</span><span class="sxs-lookup"><span data-stu-id="e8c03-105">NM\_RDBLCLK (list view) notification code</span></span>

<span data-ttu-id="e8c03-106">Посылается элементом управления "представление списка", когда пользователь дважды щелкает элемент с правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="e8c03-106">Sent by a list-view control when the user double-clicks an item with the right mouse button.</span></span> <span data-ttu-id="e8c03-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c03-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e8c03-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8c03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8c03-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c03-110">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e8c03-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="e8c03-111">Указатель на структуру [**нмитемактивате**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="e8c03-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="e8c03-112">Члены этой структуры **Член iItem**, **iSubItem** и **птактион** содержат сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="e8c03-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c03-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8c03-113">Return value</span></span>

<span data-ttu-id="e8c03-114">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="e8c03-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c03-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8c03-115">Remarks</span></span>

<span data-ttu-id="e8c03-116">Член **Член iItem** класса *lParam* допустим только в том случае, если была нажата метка значка или первого столбца.</span><span class="sxs-lookup"><span data-stu-id="e8c03-116">The **iItem** member of *lParam* is valid only if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="e8c03-117">Чтобы определить, какой элемент выбран при нажатии на другое место в строке, отправьте сообщение [**LVM \_ субитемхиттест**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c03-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c03-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e8c03-118">Requirements</span></span>



| <span data-ttu-id="e8c03-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e8c03-119">Requirement</span></span> | <span data-ttu-id="e8c03-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e8c03-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c03-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8c03-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c03-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8c03-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8c03-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8c03-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c03-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8c03-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8c03-125">Header</span><span class="sxs-lookup"><span data-stu-id="e8c03-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8c03-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8c03-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





