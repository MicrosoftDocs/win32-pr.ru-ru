---
title: Код уведомления NM_DBLCLK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул левую кнопку мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Элементы управления Windows для кода уведомления NM_DBLCLK (TAB)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137082"
---
# <a name="nm_dblclk-tab-notification-code"></a><span data-ttu-id="191f5-105">\_Код уведомления "NM дблклк (вкладка)"</span><span class="sxs-lookup"><span data-stu-id="191f5-105">NM\_DBLCLK (tab) notification code</span></span>

<span data-ttu-id="191f5-106">Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул левую кнопку мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="191f5-106">Notifies a parent window of a tab control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="191f5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="191f5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="191f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="191f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="191f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="191f5-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="191f5-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="191f5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="191f5-111">Return value</span></span>

<span data-ttu-id="191f5-112">Возвращает ненулевое значение, чтобы не разрешать обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="191f5-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="191f5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="191f5-113">Requirements</span></span>



| <span data-ttu-id="191f5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="191f5-114">Requirement</span></span> | <span data-ttu-id="191f5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="191f5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="191f5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="191f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="191f5-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="191f5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="191f5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="191f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="191f5-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="191f5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="191f5-120">Header</span><span class="sxs-lookup"><span data-stu-id="191f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="191f5-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="191f5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





