---
title: Код уведомления NM_KILLFOCUS (представление списка) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент управления потерял фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- Элементы управления Windows для кода уведомления NM_KILLFOCUS (представление списка)
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c031f3ab23d9f79ccf7f29dcfdf5472162214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489039"
---
# <a name="nm_killfocus-list-view-notification-code"></a><span data-ttu-id="ed1b7-105">\_Код уведомления NM киллфокус (представление списка)</span><span class="sxs-lookup"><span data-stu-id="ed1b7-105">NM\_KILLFOCUS (list view) notification code</span></span>

<span data-ttu-id="ed1b7-106">Сообщает родительскому окну элемента управления "представление списка", что элемент управления потерял фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="ed1b7-106">Notifies a list-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="ed1b7-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ed1b7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed1b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed1b7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1b7-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="ed1b7-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1b7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed1b7-111">Return value</span></span>

<span data-ttu-id="ed1b7-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="ed1b7-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1b7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ed1b7-113">Requirements</span></span>



| <span data-ttu-id="ed1b7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ed1b7-114">Requirement</span></span> | <span data-ttu-id="ed1b7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ed1b7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1b7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed1b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1b7-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed1b7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed1b7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed1b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1b7-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed1b7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed1b7-120">Header</span><span class="sxs-lookup"><span data-stu-id="ed1b7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1b7-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





