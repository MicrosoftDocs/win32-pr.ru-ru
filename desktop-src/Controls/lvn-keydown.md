---
title: Код уведомления LVN_KEYDOWN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что была нажата клавиша. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- LVN_KEYDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989446"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="fe5de-105">\_Код уведомления ЛВН KeyDown</span><span class="sxs-lookup"><span data-stu-id="fe5de-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="fe5de-106">Сообщает родительскому окну элемента управления "представление списка", что была нажата клавиша.</span><span class="sxs-lookup"><span data-stu-id="fe5de-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="fe5de-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5de-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fe5de-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe5de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe5de-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe5de-110">Указатель на структуру [**нмлвкэйдовн**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="fe5de-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5de-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe5de-111">Return value</span></span>

<span data-ttu-id="fe5de-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fe5de-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5de-113">Требования</span><span class="sxs-lookup"><span data-stu-id="fe5de-113">Requirements</span></span>



| <span data-ttu-id="fe5de-114">Требование</span><span class="sxs-lookup"><span data-stu-id="fe5de-114">Requirement</span></span> | <span data-ttu-id="fe5de-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fe5de-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5de-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe5de-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5de-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe5de-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe5de-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe5de-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5de-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe5de-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe5de-120">Header</span><span class="sxs-lookup"><span data-stu-id="fe5de-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe5de-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe5de-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





