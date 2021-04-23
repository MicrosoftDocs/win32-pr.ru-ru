---
title: Код уведомления LVN_HOTTRACK (Коммктрл. h)
description: Посылается элементом управления "представление списка", когда пользователь перемещает указатель мыши на элемент. Этот код уведомления отправляется только элементами управления "представление списка", имеющим \_ \_ Расширенный стиль представления списка LVS ex траккселект. Он отправляется в виде \_ сообщения WM notify.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892826"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="7e14c-106">\_Код уведомления ЛВН хоттракк</span><span class="sxs-lookup"><span data-stu-id="7e14c-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="7e14c-107">Посылается элементом управления "представление списка", когда пользователь перемещает указатель мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="7e14c-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="7e14c-108">Этот код уведомления отправляется только элементами управления "представление списка", имеющим расширенный стиль представления списка [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7e14c-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="7e14c-109">Он отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7e14c-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7e14c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e14c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e14c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e14c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e14c-112">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="7e14c-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="7e14c-113">Члены этой структуры **Член iItem**, **iSubItem** и **птактион** содержат сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="7e14c-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="7e14c-114">Принимающее приложение может изменить элемент **Член iItem** , чтобы указать элемент, который будет выбран.</span><span class="sxs-lookup"><span data-stu-id="7e14c-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="7e14c-115">Если для **Член iItem** задано значение-1, элемент не будет выбран.</span><span class="sxs-lookup"><span data-stu-id="7e14c-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e14c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e14c-116">Return value</span></span>

<span data-ttu-id="7e14c-117">Возвращает ноль, чтобы позволить представлению списка выполнять нормальную обработку выбора.</span><span class="sxs-lookup"><span data-stu-id="7e14c-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="7e14c-118">Если приложение возвращает ненулевое значение, элемент не будет выбран.</span><span class="sxs-lookup"><span data-stu-id="7e14c-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e14c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7e14c-119">Requirements</span></span>



| <span data-ttu-id="7e14c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7e14c-120">Requirement</span></span> | <span data-ttu-id="7e14c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7e14c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e14c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e14c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e14c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e14c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e14c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e14c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e14c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e14c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e14c-126">Header</span><span class="sxs-lookup"><span data-stu-id="7e14c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e14c-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e14c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





