---
title: Код уведомления LVN_INSERTITEM (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что был вставлен новый элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493329"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="16545-105">\_Код уведомления ЛВН INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="16545-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="16545-106">Сообщает родительскому окну элемента управления "представление списка", что был вставлен новый элемент.</span><span class="sxs-lookup"><span data-stu-id="16545-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="16545-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="16545-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="16545-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="16545-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16545-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16545-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16545-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="16545-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="16545-111">Член **Член iItem** определяет новый элемент, а остальные члены равны нулю.</span><span class="sxs-lookup"><span data-stu-id="16545-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16545-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16545-112">Return value</span></span>

<span data-ttu-id="16545-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="16545-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="16545-114">Требования</span><span class="sxs-lookup"><span data-stu-id="16545-114">Requirements</span></span>



| <span data-ttu-id="16545-115">Требование</span><span class="sxs-lookup"><span data-stu-id="16545-115">Requirement</span></span> | <span data-ttu-id="16545-116">Значение</span><span class="sxs-lookup"><span data-stu-id="16545-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16545-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16545-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16545-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16545-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16545-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16545-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16545-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16545-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16545-121">Header</span><span class="sxs-lookup"><span data-stu-id="16545-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="16545-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="16545-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





