---
title: Код уведомления LVN_GETINFOTIP (Коммктрл. h)
description: Отправляется элементом управления "представление списка" с большим значком, имеющим \_ \_ Расширенный стиль подсказки LVS ex.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535645"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="8342a-104">\_Код уведомления ЛВН жетинфотип</span><span class="sxs-lookup"><span data-stu-id="8342a-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="8342a-105">Отправляется элементом управления "представление списка" с большим значком, имеющим расширенный стиль [**\_ \_ подсказки LVS ex**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8342a-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="8342a-106">Этот код уведомления отправляется, когда элемент управления "представление списка" запрашивает дополнительную текстовую информацию для отображения в подсказке.</span><span class="sxs-lookup"><span data-stu-id="8342a-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="8342a-107">Он отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8342a-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8342a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8342a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8342a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8342a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8342a-110">Указатель на структуру [**нмлвжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="8342a-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8342a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8342a-111">Return value</span></span>

<span data-ttu-id="8342a-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="8342a-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8342a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8342a-113">Remarks</span></span>

<span data-ttu-id="8342a-114">Этот код уведомления отправляется только элементами управления "представление списка", у которых есть расширенный стиль [**\_ \_ подсказки LVS ex**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8342a-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="8342a-115">\_Код уведомления ЛВН жетинфотип отправляется только для подэлемента 0.</span><span class="sxs-lookup"><span data-stu-id="8342a-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="8342a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8342a-116">Requirements</span></span>



| <span data-ttu-id="8342a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8342a-117">Requirement</span></span> | <span data-ttu-id="8342a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8342a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8342a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8342a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8342a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8342a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8342a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8342a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8342a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8342a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8342a-123">Header</span><span class="sxs-lookup"><span data-stu-id="8342a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8342a-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8342a-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8342a-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8342a-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8342a-126">**ЛВН \_ ЖЕТИНФОТИПВ** (Юникод) и **ЛВН \_ жетинфотипа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8342a-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





