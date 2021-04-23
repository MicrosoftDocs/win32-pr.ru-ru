---
title: Код уведомления NM_DBLCLK (в виде дерева) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что пользователь дважды щелкнул левую кнопку мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- Элементы управления Windows для кода уведомления NM_DBLCLK (представление в виде дерева)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071112"
---
# <a name="nm_dblclk-tree-view-notification-code"></a><span data-ttu-id="e39ac-105">\_Код уведомления NM дблклк (в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="e39ac-105">NM\_DBLCLK (tree view) notification code</span></span>

<span data-ttu-id="e39ac-106">Сообщает родительскому окну элемента управления иерархического представления о том, что пользователь дважды щелкнул левую кнопку мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="e39ac-106">Notifies the parent window of a tree-view control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="e39ac-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e39ac-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e39ac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e39ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e39ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e39ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e39ac-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="e39ac-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e39ac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e39ac-111">Return value</span></span>

<span data-ttu-id="e39ac-112">Возвращает ненулевое значение, чтобы предотвратить обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e39ac-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e39ac-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e39ac-113">Requirements</span></span>



| <span data-ttu-id="e39ac-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e39ac-114">Requirement</span></span> | <span data-ttu-id="e39ac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e39ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e39ac-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e39ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e39ac-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e39ac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e39ac-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e39ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e39ac-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e39ac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e39ac-120">Header</span><span class="sxs-lookup"><span data-stu-id="e39ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e39ac-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e39ac-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





