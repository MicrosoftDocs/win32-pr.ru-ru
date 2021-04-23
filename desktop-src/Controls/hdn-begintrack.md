---
title: Код уведомления HDN_BEGINTRACK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь начал перетаскивание разделителя в элементе управления (т. е. пользователь нажал левую кнопку мыши, когда курсор мыши находится на разделителе в элементе управления "заголовок").
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137902"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="68cba-104">\_Код уведомления ХДН бегинтракк</span><span class="sxs-lookup"><span data-stu-id="68cba-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="68cba-105">Сообщает родительскому окну элемента управления заголовка, что пользователь начал перетаскивание разделителя в элементе управления (т. е. пользователь нажал левую кнопку мыши, когда курсор мыши находится на разделителе в элементе управления "заголовок").</span><span class="sxs-lookup"><span data-stu-id="68cba-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="68cba-106">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="68cba-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="68cba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="68cba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68cba-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68cba-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68cba-109">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления заголовка и элементе, разделитель которого нужно перетащить.</span><span class="sxs-lookup"><span data-stu-id="68cba-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68cba-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68cba-110">Return value</span></span>

<span data-ttu-id="68cba-111">Возвращает **значение false** , чтобы разрешить отслеживание разделителя, или **значение true** , чтобы предотвратить отслеживание.</span><span class="sxs-lookup"><span data-stu-id="68cba-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="68cba-112">Требования</span><span class="sxs-lookup"><span data-stu-id="68cba-112">Requirements</span></span>



| <span data-ttu-id="68cba-113">Требование</span><span class="sxs-lookup"><span data-stu-id="68cba-113">Requirement</span></span> | <span data-ttu-id="68cba-114">Значение</span><span class="sxs-lookup"><span data-stu-id="68cba-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68cba-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68cba-115">Minimum supported client</span></span><br/> | <span data-ttu-id="68cba-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68cba-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68cba-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68cba-117">Minimum supported server</span></span><br/> | <span data-ttu-id="68cba-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68cba-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68cba-119">Header</span><span class="sxs-lookup"><span data-stu-id="68cba-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="68cba-120"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="68cba-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="68cba-121">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="68cba-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="68cba-122">**ХДН \_ БЕГИНТРАККВ** (Юникод) и **ХДН \_ бегинтракка** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="68cba-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 





