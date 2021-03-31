---
title: Код уведомления HDN_ENDTRACK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь завершил перетаскивание разделителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071198"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="3edd6-105">\_Код уведомления ХДН ендтракк</span><span class="sxs-lookup"><span data-stu-id="3edd6-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="3edd6-106">Сообщает родительскому окну элемента управления заголовка, что пользователь завершил перетаскивание разделителя.</span><span class="sxs-lookup"><span data-stu-id="3edd6-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="3edd6-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3edd6-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3edd6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3edd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3edd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3edd6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3edd6-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления заголовка и элементе, разделитель которого был перетащен.</span><span class="sxs-lookup"><span data-stu-id="3edd6-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3edd6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3edd6-111">Return value</span></span>

<span data-ttu-id="3edd6-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3edd6-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3edd6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3edd6-113">Requirements</span></span>



| <span data-ttu-id="3edd6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3edd6-114">Requirement</span></span> | <span data-ttu-id="3edd6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3edd6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3edd6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3edd6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3edd6-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3edd6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3edd6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3edd6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3edd6-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3edd6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3edd6-120">Header</span><span class="sxs-lookup"><span data-stu-id="3edd6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3edd6-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3edd6-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3edd6-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3edd6-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3edd6-123">**ХДН \_ ЕНДТРАККВ** (Юникод) и **ХДН \_ ендтракка** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3edd6-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 





