---
title: Код уведомления NM_RELEASEDCAPTURE (TrackBar) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления TrackBar, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 1e3e4f67-672d-4e3e-84f4-b3fa6221d118
keywords:
- Элементы управления Windows для кода уведомления NM_RELEASEDCAPTURE (TrackBar)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684f58fb5328cfe0d25fc73ce7c1a2d9a189d86f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136842"
---
# <a name="nm_releasedcapture-trackbar-notification-code"></a><span data-ttu-id="ae143-105">\_Код уведомления NM релеаседкаптуре (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="ae143-105">NM\_RELEASEDCAPTURE (trackbar) notification code</span></span>

<span data-ttu-id="ae143-106">Сообщает родительскому окну элемента управления TrackBar, что элемент управления освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="ae143-106">Notifies a trackbar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="ae143-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ae143-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ae143-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae143-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae143-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae143-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="ae143-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae143-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae143-111">Return value</span></span>

<span data-ttu-id="ae143-112">Элемент управления игнорирует возвращаемое значение из этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="ae143-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae143-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ae143-113">Requirements</span></span>



| <span data-ttu-id="ae143-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ae143-114">Requirement</span></span> | <span data-ttu-id="ae143-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ae143-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae143-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae143-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ae143-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae143-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae143-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae143-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ae143-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae143-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae143-120">Header</span><span class="sxs-lookup"><span data-stu-id="ae143-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae143-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae143-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





