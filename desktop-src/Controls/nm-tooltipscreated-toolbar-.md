---
title: Код уведомления NM_TOOLTIPSCREATED (Toolbar) (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что панель инструментов создала элемент управления ToolTip. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Элементы управления Windows для кода уведомления NM_TOOLTIPSCREATED (панель инструментов)
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489954"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a><span data-ttu-id="28c6a-105">\_Код уведомления "NM тултипскреатед (панель инструментов)"</span><span class="sxs-lookup"><span data-stu-id="28c6a-105">NM\_TOOLTIPSCREATED (toolbar) notification code</span></span>

<span data-ttu-id="28c6a-106">Сообщает родительскому окну панели инструментов, что панель инструментов создала элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="28c6a-106">Notifies a toolbar's parent window that the toolbar has created a tooltip control.</span></span> <span data-ttu-id="28c6a-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="28c6a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="28c6a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="28c6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c6a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28c6a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28c6a-110">Указатель на структуру [**нмтултипскреатед**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="28c6a-110">Pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c6a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28c6a-111">Return value</span></span>

<span data-ttu-id="28c6a-112">Элемент управления ToolBar игнорирует возвращаемое значение из этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="28c6a-112">The toolbar control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c6a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="28c6a-113">Requirements</span></span>



| <span data-ttu-id="28c6a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="28c6a-114">Requirement</span></span> | <span data-ttu-id="28c6a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="28c6a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28c6a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28c6a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28c6a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28c6a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28c6a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28c6a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28c6a-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28c6a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28c6a-120">Header</span><span class="sxs-lookup"><span data-stu-id="28c6a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c6a-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c6a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





