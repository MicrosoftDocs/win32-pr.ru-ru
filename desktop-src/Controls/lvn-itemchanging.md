---
title: Код уведомления LVN_ITEMCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент изменяется. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989447"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="cb37a-105">\_Код уведомления ЛВН итемчангинг</span><span class="sxs-lookup"><span data-stu-id="cb37a-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="cb37a-106">Сообщает родительскому окну элемента управления "представление списка", что элемент изменяется.</span><span class="sxs-lookup"><span data-stu-id="cb37a-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="cb37a-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cb37a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cb37a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb37a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb37a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb37a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb37a-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) , которая идентифицирует элемент и указывает, какие из его атрибутов изменяются.</span><span class="sxs-lookup"><span data-stu-id="cb37a-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb37a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb37a-111">Return value</span></span>

<span data-ttu-id="cb37a-112">Возвращает **значение true** , чтобы предотвратить изменение, или **false** , чтобы разрешить изменение.</span><span class="sxs-lookup"><span data-stu-id="cb37a-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb37a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb37a-113">Remarks</span></span>

<span data-ttu-id="cb37a-114">Если элемент управления "представление списка" имеет стиль [**LVS \_ ОВНЕРДАТА**](list-view-window-styles.md) , ЛВН \_ итемчангинг коды уведомлений не отправляются.</span><span class="sxs-lookup"><span data-stu-id="cb37a-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb37a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cb37a-115">Requirements</span></span>



| <span data-ttu-id="cb37a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cb37a-116">Requirement</span></span> | <span data-ttu-id="cb37a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cb37a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb37a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb37a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb37a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb37a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb37a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb37a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb37a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb37a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb37a-122">Header</span><span class="sxs-lookup"><span data-stu-id="cb37a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb37a-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb37a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





