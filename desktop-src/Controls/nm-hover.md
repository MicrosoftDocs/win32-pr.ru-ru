---
title: Код уведомления NM_HOVER (Коммктрл. h)
description: Посылается элементом управления при наведении указателя мыши на элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- NM_HOVER кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801096"
---
# <a name="nm_hover-notification-code"></a><span data-ttu-id="7fa1c-105">\_Код уведомления о наведении в NM</span><span class="sxs-lookup"><span data-stu-id="7fa1c-105">NM\_HOVER notification code</span></span>

<span data-ttu-id="7fa1c-106">Посылается элементом управления при наведении указателя мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-106">Sent by a control when the mouse hovers over an item.</span></span> <span data-ttu-id="7fa1c-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa1c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7fa1c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fa1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa1c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fa1c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fa1c-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa1c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fa1c-111">Return value</span></span>

<span data-ttu-id="7fa1c-112">Если не указано иное, возвращается нуль, чтобы разрешить элементу управления обрабатываться в обычном режиме, или ненулевой, чтобы предотвратить обработку наведения.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-112">Unless otherwise specified, return zero to allow the control to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa1c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7fa1c-113">Requirements</span></span>



| <span data-ttu-id="7fa1c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7fa1c-114">Requirement</span></span> | <span data-ttu-id="7fa1c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7fa1c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa1c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fa1c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa1c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fa1c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fa1c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fa1c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa1c-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fa1c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fa1c-120">Header</span><span class="sxs-lookup"><span data-stu-id="7fa1c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fa1c-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa1c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





