---
title: Код уведомления TTN_POP (Коммктрл. h)
description: Сообщает окну-владельцу, что всплывающая подсказка будет скрыта. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- TTN_POP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802236"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="b3e13-105">\_Код уведомления POP ТТН</span><span class="sxs-lookup"><span data-stu-id="b3e13-105">TTN\_POP notification code</span></span>

<span data-ttu-id="b3e13-106">Сообщает окну-владельцу, что всплывающая подсказка будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="b3e13-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="b3e13-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b3e13-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b3e13-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3e13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3e13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e13-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="b3e13-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e13-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3e13-111">Return value</span></span>

<span data-ttu-id="b3e13-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b3e13-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e13-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b3e13-113">Requirements</span></span>



| <span data-ttu-id="b3e13-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b3e13-114">Requirement</span></span> | <span data-ttu-id="b3e13-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b3e13-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e13-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3e13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e13-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3e13-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3e13-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3e13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e13-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3e13-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3e13-120">Header</span><span class="sxs-lookup"><span data-stu-id="b3e13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3e13-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e13-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





