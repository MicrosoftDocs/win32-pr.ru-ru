---
title: Код уведомления NM_RETURN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элемент управления имеет фокус ввода и что пользователь нажал клавишу ВВОД. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- NM_RETURN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534841"
---
# <a name="nm_return-notification-code"></a><span data-ttu-id="fcf22-105">\_Код уведомления о возврате для NM</span><span class="sxs-lookup"><span data-stu-id="fcf22-105">NM\_RETURN notification code</span></span>

<span data-ttu-id="fcf22-106">Сообщает родительскому окну элемента управления, что элемент управления имеет фокус ввода и что пользователь нажал клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="fcf22-106">Notifies a control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="fcf22-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fcf22-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fcf22-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcf22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf22-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcf22-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcf22-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="fcf22-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf22-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcf22-111">Return value</span></span>

<span data-ttu-id="fcf22-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="fcf22-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf22-113">Требования</span><span class="sxs-lookup"><span data-stu-id="fcf22-113">Requirements</span></span>



| <span data-ttu-id="fcf22-114">Требование</span><span class="sxs-lookup"><span data-stu-id="fcf22-114">Requirement</span></span> | <span data-ttu-id="fcf22-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fcf22-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcf22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf22-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcf22-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcf22-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcf22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf22-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcf22-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcf22-120">Header</span><span class="sxs-lookup"><span data-stu-id="fcf22-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf22-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf22-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





