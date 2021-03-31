---
title: Код уведомления TVN_SELCHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что выделение изменилось с одного элемента на другой. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892598"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="88807-105">\_Код уведомления ТВН селчанжед</span><span class="sxs-lookup"><span data-stu-id="88807-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="88807-106">Сообщает родительскому окну элемента управления древовидного представления о том, что выделение изменилось с одного элемента на другой.</span><span class="sxs-lookup"><span data-stu-id="88807-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="88807-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="88807-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="88807-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="88807-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88807-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88807-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88807-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="88807-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="88807-111">Элементы **итемолд** и **итемнев** структуры **нмтривиев** представляют собой [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) структуры, содержащие сведения о ранее выбранном элементе и вновь выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="88807-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="88807-112">Допустимы только члены **масок**, **хитем**, **State** и **lParam** этих структур.</span><span class="sxs-lookup"><span data-stu-id="88807-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="88807-113">Элементы **статемаск** структур **твитем** , заданные с помощью **итемолд** и **итемнев** , не определены на входе.</span><span class="sxs-lookup"><span data-stu-id="88807-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="88807-114">Элемент **Action** структуры **нмтривиев** указывает тип действия, вызвавшего изменение выбора.</span><span class="sxs-lookup"><span data-stu-id="88807-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="88807-115">Может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="88807-115">It can be one of the following values:</span></span>



| <span data-ttu-id="88807-116">Требование</span><span class="sxs-lookup"><span data-stu-id="88807-116">Requirement</span></span> | <span data-ttu-id="88807-117">Значение</span><span class="sxs-lookup"><span data-stu-id="88807-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="88807-118">ТВК \_ бикэйбоард</span><span class="sxs-lookup"><span data-stu-id="88807-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="88807-119">Нажатием клавиши.</span><span class="sxs-lookup"><span data-stu-id="88807-119">By a keystroke.</span></span>   |
| <span data-ttu-id="88807-120">ТВК \_ бимаусе</span><span class="sxs-lookup"><span data-stu-id="88807-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="88807-121">Щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="88807-121">By a mouse click.</span></span> |
| <span data-ttu-id="88807-122">ТВК \_ неизвестный</span><span class="sxs-lookup"><span data-stu-id="88807-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="88807-123">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="88807-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88807-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88807-124">Return value</span></span>

<span data-ttu-id="88807-125">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="88807-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="88807-126">Требования</span><span class="sxs-lookup"><span data-stu-id="88807-126">Requirements</span></span>



| <span data-ttu-id="88807-127">Требование</span><span class="sxs-lookup"><span data-stu-id="88807-127">Requirement</span></span> | <span data-ttu-id="88807-128">Значение</span><span class="sxs-lookup"><span data-stu-id="88807-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88807-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88807-129">Minimum supported client</span></span><br/> | <span data-ttu-id="88807-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88807-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88807-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88807-131">Minimum supported server</span></span><br/> | <span data-ttu-id="88807-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="88807-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88807-133">Header</span><span class="sxs-lookup"><span data-stu-id="88807-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="88807-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="88807-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="88807-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="88807-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="88807-136">**ТВН \_ СЕЛЧАНЖЕДВ** (Юникод) и **ТВН \_ селчанжеда** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="88807-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





