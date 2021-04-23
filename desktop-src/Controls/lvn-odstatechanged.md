---
title: Код уведомления LVN_ODSTATECHANGED (Коммктрл. h)
description: Отправляется элементом управления "представление списка" при изменении состояния элемента или диапазона элементов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803064"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="90b7a-105">\_Код уведомления ЛВН одстатечанжед</span><span class="sxs-lookup"><span data-stu-id="90b7a-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="90b7a-106">Отправляется элементом управления "представление списка" при изменении состояния элемента или диапазона элементов.</span><span class="sxs-lookup"><span data-stu-id="90b7a-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="90b7a-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90b7a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="90b7a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90b7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90b7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90b7a-110">Указатель на структуру [**нмлводстатечанже**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) , которая содержит сведения об измененном элементе или элементах.</span><span class="sxs-lookup"><span data-stu-id="90b7a-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b7a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90b7a-111">Return value</span></span>

<span data-ttu-id="90b7a-112">Приложение, получающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="90b7a-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="90b7a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="90b7a-113">Requirements</span></span>



| <span data-ttu-id="90b7a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="90b7a-114">Requirement</span></span> | <span data-ttu-id="90b7a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="90b7a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90b7a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90b7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90b7a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90b7a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90b7a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90b7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90b7a-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90b7a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90b7a-120">Header</span><span class="sxs-lookup"><span data-stu-id="90b7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90b7a-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="90b7a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





