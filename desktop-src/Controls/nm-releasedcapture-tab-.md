---
title: Код уведомления NM_RELEASEDCAPTURE (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления вкладки, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- Элементы управления Windows для кода уведомления NM_RELEASEDCAPTURE (TAB)
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
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491445"
---
# <a name="nm_releasedcapture-tab-notification-code"></a><span data-ttu-id="ff2dd-105">\_Код уведомления "NM релеаседкаптуре (вкладка)"</span><span class="sxs-lookup"><span data-stu-id="ff2dd-105">NM\_RELEASEDCAPTURE (tab) notification code</span></span>

<span data-ttu-id="ff2dd-106">Сообщает родительскому окну элемента управления вкладки, что элемент управления освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-106">Notifies a tab control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="ff2dd-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ff2dd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ff2dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff2dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff2dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff2dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff2dd-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff2dd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff2dd-111">Return value</span></span>

<span data-ttu-id="ff2dd-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff2dd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ff2dd-113">Requirements</span></span>



| <span data-ttu-id="ff2dd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ff2dd-114">Requirement</span></span> | <span data-ttu-id="ff2dd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ff2dd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2dd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff2dd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff2dd-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff2dd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff2dd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff2dd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff2dd-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff2dd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff2dd-120">Header</span><span class="sxs-lookup"><span data-stu-id="ff2dd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff2dd-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff2dd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





