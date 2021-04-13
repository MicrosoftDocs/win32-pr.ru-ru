---
title: Код уведомления NM_RCLICK (строка состояния) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "строка состояния", что пользователь щелкнул правой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- Элементы управления Windows для кода уведомления NM_RCLICK (строка состояния)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341370"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="3c12d-105">\_Код уведомления NM ркликк (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="3c12d-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="3c12d-106">Сообщает родительскому окну элемента управления "строка состояния", что пользователь щелкнул правой кнопкой мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="3c12d-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="3c12d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3c12d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3c12d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c12d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c12d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c12d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c12d-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="3c12d-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c12d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c12d-111">Return value</span></span>

<span data-ttu-id="3c12d-112">Возвращает **значение true** , чтобы указать, что нажатие кнопки мыши было обработано, и подавить обработку по умолчанию системой.</span><span class="sxs-lookup"><span data-stu-id="3c12d-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="3c12d-113">Возвращает **значение false** , чтобы разрешить обработку по умолчанию щелчка.</span><span class="sxs-lookup"><span data-stu-id="3c12d-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c12d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3c12d-114">Requirements</span></span>



| <span data-ttu-id="3c12d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3c12d-115">Requirement</span></span> | <span data-ttu-id="3c12d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3c12d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c12d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c12d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c12d-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c12d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c12d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c12d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c12d-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c12d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c12d-121">Header</span><span class="sxs-lookup"><span data-stu-id="3c12d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c12d-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c12d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





