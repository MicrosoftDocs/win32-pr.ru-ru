---
title: Код уведомления NM_DBLCLK (строка состояния) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "строка состояния", что пользователь дважды щелкнул левую кнопку мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- Элементы управления Windows для кода уведомления NM_DBLCLK (строка состояния)
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
ms.openlocfilehash: 28866effbc4143dc9d0d5a3800f88711c99f88db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988194"
---
# <a name="nm_dblclk-status-bar-notification-code"></a><span data-ttu-id="5f09f-105">\_Код уведомления NM дблклк (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="5f09f-105">NM\_DBLCLK (status bar) notification code</span></span>

<span data-ttu-id="5f09f-106">Сообщает родительскому окну элемента управления "строка состояния", что пользователь дважды щелкнул левую кнопку мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="5f09f-106">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="5f09f-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5f09f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5f09f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f09f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f09f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f09f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f09f-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="5f09f-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="5f09f-111">Элемент **двитемспек** содержит индекс раздела, который был выбран.</span><span class="sxs-lookup"><span data-stu-id="5f09f-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f09f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f09f-112">Return value</span></span>

<span data-ttu-id="5f09f-113">Возвращает **значение true** , чтобы указать, что нажатие кнопки мыши было обработано, и подавить обработку по умолчанию системой.</span><span class="sxs-lookup"><span data-stu-id="5f09f-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="5f09f-114">Возвращает **значение false** , чтобы разрешить обработку по умолчанию щелчка.</span><span class="sxs-lookup"><span data-stu-id="5f09f-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f09f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5f09f-115">Requirements</span></span>



| <span data-ttu-id="5f09f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5f09f-116">Requirement</span></span> | <span data-ttu-id="5f09f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5f09f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f09f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f09f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f09f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f09f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f09f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f09f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f09f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f09f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f09f-122">Header</span><span class="sxs-lookup"><span data-stu-id="5f09f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f09f-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f09f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





