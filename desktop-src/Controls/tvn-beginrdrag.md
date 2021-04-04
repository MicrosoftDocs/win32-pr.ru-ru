---
title: Код уведомления TVN_BEGINRDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления об инициации операции перетаскивания, включающей правую кнопку мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989279"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="32275-105">\_Код уведомления ТВН бегинрдраг</span><span class="sxs-lookup"><span data-stu-id="32275-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="32275-106">Сообщает родительскому окну элемента управления иерархического представления об инициации операции перетаскивания, включающей правую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="32275-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="32275-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="32275-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="32275-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="32275-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32275-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32275-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32275-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="32275-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="32275-111">Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения в членах **хитем**, **State** и **lParam** о перемещенном элементе.</span><span class="sxs-lookup"><span data-stu-id="32275-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="32275-112">Элемент **птдраг** указывает текущие экранные координаты мыши.</span><span class="sxs-lookup"><span data-stu-id="32275-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32275-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32275-113">Return value</span></span>

<span data-ttu-id="32275-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="32275-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="32275-115">Требования</span><span class="sxs-lookup"><span data-stu-id="32275-115">Requirements</span></span>



| <span data-ttu-id="32275-116">Требование</span><span class="sxs-lookup"><span data-stu-id="32275-116">Requirement</span></span> | <span data-ttu-id="32275-117">Значение</span><span class="sxs-lookup"><span data-stu-id="32275-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32275-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32275-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32275-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32275-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32275-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32275-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32275-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32275-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32275-122">Header</span><span class="sxs-lookup"><span data-stu-id="32275-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32275-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="32275-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="32275-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="32275-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="32275-125">**ТВН \_ БЕГИНРДРАГВ** (Юникод) и **ТВН \_ бегинрдрага** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="32275-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 





