---
title: Код уведомления LVN_LINKCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что была нажата ссылка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493323"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="3b805-105">\_Код уведомления ЛВН линккликк</span><span class="sxs-lookup"><span data-stu-id="3b805-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="3b805-106">Сообщает родительскому окну элемента управления "представление списка", что была нажата ссылка.</span><span class="sxs-lookup"><span data-stu-id="3b805-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="3b805-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b805-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="3b805-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b805-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b805-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b805-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b805-110">Указатель на структуру [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) .</span><span class="sxs-lookup"><span data-stu-id="3b805-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="3b805-111">Идентификатор группы, содержащей ссылку, находится в элементе **iSubItem** .</span><span class="sxs-lookup"><span data-stu-id="3b805-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b805-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b805-112">Return value</span></span>

<span data-ttu-id="3b805-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3b805-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b805-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b805-114">Remarks</span></span>

<span data-ttu-id="3b805-115">В следующем примере показано, как приложение может реагировать на этот код уведомления в обработчике сообщений [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b805-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="3b805-116">В этом примере переключается свернутое состояние группы и устанавливается соответствующий текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="3b805-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="3b805-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3b805-117">Requirements</span></span>



| <span data-ttu-id="3b805-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3b805-118">Requirement</span></span> | <span data-ttu-id="3b805-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3b805-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b805-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b805-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b805-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b805-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b805-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b805-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b805-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b805-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b805-124">Header</span><span class="sxs-lookup"><span data-stu-id="3b805-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b805-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b805-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





