---
title: Код уведомления TCN_KEYDOWN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления вкладки, что нажата клавиша. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- TCN_KEYDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654409"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="f371c-105">\_Код уведомления ТКН KeyDown</span><span class="sxs-lookup"><span data-stu-id="f371c-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="f371c-106">Сообщает родительскому окну элемента управления вкладки, что нажата клавиша.</span><span class="sxs-lookup"><span data-stu-id="f371c-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="f371c-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f371c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f371c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f371c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f371c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f371c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f371c-110">Указатель на структуру [**нмтккэйдовн**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .</span><span class="sxs-lookup"><span data-stu-id="f371c-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f371c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f371c-111">Return value</span></span>

<span data-ttu-id="f371c-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f371c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f371c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f371c-113">Requirements</span></span>



| <span data-ttu-id="f371c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f371c-114">Requirement</span></span> | <span data-ttu-id="f371c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f371c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f371c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f371c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f371c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f371c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f371c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f371c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f371c-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f371c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f371c-120">Header</span><span class="sxs-lookup"><span data-stu-id="f371c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f371c-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f371c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





