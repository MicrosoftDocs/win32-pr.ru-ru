---
title: Код уведомления NM_THEMECHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что тема изменилась. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071816"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="c42c2-105">\_Код уведомления семечанжед (NM)</span><span class="sxs-lookup"><span data-stu-id="c42c2-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="c42c2-106">Сообщает родительскому окну элемента управления, что тема изменилась.</span><span class="sxs-lookup"><span data-stu-id="c42c2-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="c42c2-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c42c2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c42c2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c42c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c42c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c42c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c42c2-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="c42c2-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c42c2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c42c2-111">Return value</span></span>

<span data-ttu-id="c42c2-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c42c2-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c42c2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c42c2-113">Requirements</span></span>



| <span data-ttu-id="c42c2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c42c2-114">Requirement</span></span> | <span data-ttu-id="c42c2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c42c2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c42c2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c42c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c42c2-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c42c2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c42c2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c42c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c42c2-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c42c2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c42c2-120">Header</span><span class="sxs-lookup"><span data-stu-id="c42c2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c42c2-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c42c2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





