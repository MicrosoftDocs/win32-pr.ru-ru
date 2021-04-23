---
title: Код уведомления HDN_TRACK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь перетаскивает разделитель в элементе управления "заголовок". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892242"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="afd81-105">\_Код уведомления ХДН Track</span><span class="sxs-lookup"><span data-stu-id="afd81-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="afd81-106">Сообщает родительскому окну элемента управления заголовка, что пользователь перетаскивает разделитель в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="afd81-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="afd81-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="afd81-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="afd81-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="afd81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd81-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afd81-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afd81-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления заголовка и элементе, разделитель которого перетаскивается.</span><span class="sxs-lookup"><span data-stu-id="afd81-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd81-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afd81-111">Return value</span></span>

<span data-ttu-id="afd81-112">Возвращает **значение false** , чтобы продолжить отслеживание разделителя, или **true** для завершения отслеживания.</span><span class="sxs-lookup"><span data-stu-id="afd81-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd81-113">Требования</span><span class="sxs-lookup"><span data-stu-id="afd81-113">Requirements</span></span>



| <span data-ttu-id="afd81-114">Требование</span><span class="sxs-lookup"><span data-stu-id="afd81-114">Requirement</span></span> | <span data-ttu-id="afd81-115">Значение</span><span class="sxs-lookup"><span data-stu-id="afd81-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afd81-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afd81-116">Minimum supported client</span></span><br/> | <span data-ttu-id="afd81-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afd81-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afd81-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afd81-118">Minimum supported server</span></span><br/> | <span data-ttu-id="afd81-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="afd81-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afd81-120">Header</span><span class="sxs-lookup"><span data-stu-id="afd81-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="afd81-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd81-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="afd81-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="afd81-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="afd81-123">**ХДН \_ ТРАККВ** (Юникод) и **ХДН \_ Tracking** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="afd81-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 





