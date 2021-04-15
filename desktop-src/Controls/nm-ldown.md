---
title: Код уведомления NM_LDOWN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что была нажата левая кнопка мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- NM_LDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654425"
---
# <a name="nm_ldown-notification-code"></a><span data-ttu-id="4dc8c-105">\_Код уведомления лдовн (NM)</span><span class="sxs-lookup"><span data-stu-id="4dc8c-105">NM\_LDOWN notification code</span></span>

<span data-ttu-id="4dc8c-106">Сообщает родительскому окну элемента управления, что была нажата левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="4dc8c-106">Notifies a control's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="4dc8c-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4dc8c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4dc8c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dc8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc8c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dc8c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc8c-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="4dc8c-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dc8c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dc8c-111">Return value</span></span>

<span data-ttu-id="4dc8c-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="4dc8c-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc8c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4dc8c-113">Requirements</span></span>



| <span data-ttu-id="4dc8c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4dc8c-114">Requirement</span></span> | <span data-ttu-id="4dc8c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4dc8c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc8c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dc8c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc8c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4dc8c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4dc8c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dc8c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc8c-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4dc8c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4dc8c-120">Header</span><span class="sxs-lookup"><span data-stu-id="4dc8c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc8c-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc8c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





