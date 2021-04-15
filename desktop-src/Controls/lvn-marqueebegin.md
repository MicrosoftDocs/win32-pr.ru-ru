---
title: Код уведомления LVN_MARQUEEBEGIN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что началось выделение ограничивающего прямоугольника (бегущая строка). Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654730"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="858b2-105">\_Код уведомления ЛВН маркуибегин</span><span class="sxs-lookup"><span data-stu-id="858b2-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="858b2-106">Сообщает родительскому окну элемента управления "представление списка", что началось выделение ограничивающего прямоугольника (бегущая строка).</span><span class="sxs-lookup"><span data-stu-id="858b2-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="858b2-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="858b2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="858b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="858b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="858b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="858b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="858b2-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="858b2-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="858b2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="858b2-111">Return value</span></span>

<span data-ttu-id="858b2-112">Чтобы принять код уведомления, возвратите нуль.</span><span class="sxs-lookup"><span data-stu-id="858b2-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="858b2-113">Чтобы выйти из выделения ограничивающего прямоугольника, возвратите ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="858b2-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="858b2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="858b2-114">Remarks</span></span>

<span data-ttu-id="858b2-115">*Выделение ограничивающего прямоугольника* — это процесс щелчка клиентской области окна списка представлений и перетаскивания для одновременного выбора нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="858b2-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="858b2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="858b2-116">Requirements</span></span>



| <span data-ttu-id="858b2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="858b2-117">Requirement</span></span> | <span data-ttu-id="858b2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="858b2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="858b2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="858b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="858b2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="858b2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="858b2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="858b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="858b2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="858b2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="858b2-123">Header</span><span class="sxs-lookup"><span data-stu-id="858b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="858b2-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="858b2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





