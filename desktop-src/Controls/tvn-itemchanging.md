---
title: Код уведомления TVN_ITEMCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что необходимо изменить атрибуты элементов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534211"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="8e448-105">\_Код уведомления ТВН итемчангинг</span><span class="sxs-lookup"><span data-stu-id="8e448-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="8e448-106">Сообщает родительскому окну элемента управления иерархического представления о том, что необходимо изменить атрибуты элементов.</span><span class="sxs-lookup"><span data-stu-id="8e448-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="8e448-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e448-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8e448-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e448-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e448-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e448-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e448-110">Указатель на структуру [**нмтвитемчанже**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) , описывающую изменяемый элемент.</span><span class="sxs-lookup"><span data-stu-id="8e448-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="8e448-111">Для элемента **учанжед** задано состояние твиф \_ .</span><span class="sxs-lookup"><span data-stu-id="8e448-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e448-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e448-112">Return value</span></span>

<span data-ttu-id="8e448-113">Возвращает **значение false** , чтобы принять изменение, или **значение true** , чтобы предотвратить изменение.</span><span class="sxs-lookup"><span data-stu-id="8e448-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e448-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8e448-114">Requirements</span></span>



| <span data-ttu-id="8e448-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8e448-115">Requirement</span></span> | <span data-ttu-id="8e448-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e448-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e448-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e448-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e448-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e448-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e448-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e448-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e448-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e448-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e448-121">Header</span><span class="sxs-lookup"><span data-stu-id="8e448-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e448-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e448-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8e448-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8e448-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8e448-124">**ТВН \_ ИТЕМЧАНГИНГВ** (Юникод) и **ТВН \_ итемчангинга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8e448-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8e448-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e448-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e448-126">ТВН \_ итемчанжед</span><span class="sxs-lookup"><span data-stu-id="8e448-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





