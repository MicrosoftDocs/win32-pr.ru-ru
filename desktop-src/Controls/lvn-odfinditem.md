---
title: Сообщение LVN_ODFINDITEM (Коммктрл. h)
description: Отправляется виртуальным элементом управления "представление списка", когда ему требуется владелец для поиска конкретного элемента обратного вызова.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Элементы управления Windows для LVN_ODFINDITEM сообщений
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136654"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="d2239-104">\_Сообщение ЛВН одфиндитем</span><span class="sxs-lookup"><span data-stu-id="d2239-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="d2239-105">Отправляется виртуальным элементом управления " [представление списка](list-view-controls-overview.md) ", когда ему требуется владелец для поиска конкретного элемента обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d2239-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="d2239-106">Например, элемент управления будет отсылать этот код уведомления при получении сочетания клавиш для ввода с клавиатуры или при получении сообщения [**LVM \_ FINDITEM**](lvm-finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="d2239-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="d2239-107">\_Код уведомления ЛВН одфиндитем отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d2239-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d2239-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2239-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2239-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2239-110">Указатель на структуру [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , которая содержит сведения, используемые для поиска.</span><span class="sxs-lookup"><span data-stu-id="d2239-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2239-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2239-111">Return value</span></span>

<span data-ttu-id="d2239-112">Возвращает индекс найденного элемента или значение-1, если элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="d2239-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2239-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2239-113">Remarks</span></span>

<span data-ttu-id="d2239-114">Данные поиска отправляются в виде структуры [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , которая является членом структуры [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="d2239-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2239-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d2239-115">Requirements</span></span>



| <span data-ttu-id="d2239-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d2239-116">Requirement</span></span> | <span data-ttu-id="d2239-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d2239-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2239-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2239-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2239-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2239-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2239-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2239-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2239-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2239-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2239-122">Header</span><span class="sxs-lookup"><span data-stu-id="d2239-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2239-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2239-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d2239-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d2239-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d2239-125">**ЛВН \_ ОДФИНДИТЕМВ** (Юникод) и **ЛВН \_ одфиндитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d2239-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





