---
title: Код уведомления LVN_BEGINDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что инициируется операция перетаскивания, включающая левую кнопку мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071188"
---
# <a name="lvn_begindrag-notification-code"></a><span data-ttu-id="b7243-105">\_Код уведомления ЛВН бегиндраг</span><span class="sxs-lookup"><span data-stu-id="b7243-105">LVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="b7243-106">Сообщает родительскому окну элемента управления "представление списка", что инициируется операция перетаскивания, включающая левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="b7243-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="b7243-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b7243-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b7243-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7243-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7243-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7243-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7243-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="b7243-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="b7243-111">Элемент **Член iItem** определяет перетаскиваемый элемент, а остальные элементы равны нулю.</span><span class="sxs-lookup"><span data-stu-id="b7243-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7243-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7243-112">Return value</span></span>

<span data-ttu-id="b7243-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b7243-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7243-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7243-114">Requirements</span></span>



| <span data-ttu-id="b7243-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7243-115">Requirement</span></span> | <span data-ttu-id="b7243-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7243-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7243-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7243-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7243-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7243-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7243-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7243-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7243-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7243-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7243-121">Header</span><span class="sxs-lookup"><span data-stu-id="b7243-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7243-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7243-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





