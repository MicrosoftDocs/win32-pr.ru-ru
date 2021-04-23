---
title: NM_RELEASEDCAPTURE (вверх-вниз) код уведомления (Коммктрл. h)
description: Уведомляет родительского окна элемента управления, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 88a4a9a2-ba7f-4ccc-b5bf-749f49dc666b
keywords:
- Элементы управления Windows с кодом уведомления NM_RELEASEDCAPTURE (вверх-вниз)
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
ms.openlocfilehash: 4b94f2a61727861cbf47720a41c7255763992b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654609"
---
# <a name="nm_releasedcapture-up-down-notification-code"></a><span data-ttu-id="62e28-105">\_Релеаседкаптуреный код уведомления (вверх-вниз)</span><span class="sxs-lookup"><span data-stu-id="62e28-105">NM\_RELEASEDCAPTURE (up-down) notification code</span></span>

<span data-ttu-id="62e28-106">Уведомляет родительского окна элемента управления, что элемент управления освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="62e28-106">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="62e28-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="62e28-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="62e28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62e28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62e28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62e28-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="62e28-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62e28-111">Return value</span></span>

<span data-ttu-id="62e28-112">Элемент управления игнорирует возвращаемое значение из этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="62e28-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e28-113">Требования</span><span class="sxs-lookup"><span data-stu-id="62e28-113">Requirements</span></span>



| <span data-ttu-id="62e28-114">Требование</span><span class="sxs-lookup"><span data-stu-id="62e28-114">Requirement</span></span> | <span data-ttu-id="62e28-115">Значение</span><span class="sxs-lookup"><span data-stu-id="62e28-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62e28-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62e28-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62e28-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62e28-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62e28-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62e28-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62e28-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62e28-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62e28-120">Header</span><span class="sxs-lookup"><span data-stu-id="62e28-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e28-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e28-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





