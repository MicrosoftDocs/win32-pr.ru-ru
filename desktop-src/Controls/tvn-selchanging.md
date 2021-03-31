---
title: Код уведомления TVN_SELCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что выбор собирается измениться с одного элемента на другой. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071512"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="6c6e5-105">\_Код уведомления ТВН селчангинг</span><span class="sxs-lookup"><span data-stu-id="6c6e5-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="6c6e5-106">Сообщает родительскому окну элемента управления древовидного представления о том, что выбор собирается измениться с одного элемента на другой.</span><span class="sxs-lookup"><span data-stu-id="6c6e5-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="6c6e5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6c6e5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="6c6e5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c6e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6e5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c6e5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c6e5-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="6c6e5-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="6c6e5-111">Члены **итемолд** и **итемнев** содержат действительные сведения о текущем выбранном элементе и вновь выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="6c6e5-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="6c6e5-112">Член **действия** указывает, вызывает ли действие мыши или клавиатуры изменение выбора.</span><span class="sxs-lookup"><span data-stu-id="6c6e5-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="6c6e5-113">Список возможных значений см. в описании кода уведомления [ТВН \_ селчанжед](tvn-selchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="6c6e5-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6e5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c6e5-114">Return value</span></span>

<span data-ttu-id="6c6e5-115">Возвращает **значение true** , чтобы предотвратить изменение выбора.</span><span class="sxs-lookup"><span data-stu-id="6c6e5-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6e5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c6e5-116">Remarks</span></span>

<span data-ttu-id="6c6e5-117">При ответе на этот код уведомления приложения не должны удалять элементы, которые получают или теряют выбор.</span><span class="sxs-lookup"><span data-stu-id="6c6e5-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6e5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6c6e5-118">Requirements</span></span>



| <span data-ttu-id="6c6e5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6c6e5-119">Requirement</span></span> | <span data-ttu-id="6c6e5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6c6e5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6e5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c6e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6e5-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c6e5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c6e5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c6e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6e5-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c6e5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c6e5-125">Header</span><span class="sxs-lookup"><span data-stu-id="6c6e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c6e5-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6e5-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6c6e5-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6c6e5-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c6e5-128">**ТВН \_ СЕЛЧАНГИНГВ** (Юникод) и **ТВН \_ селчангинга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c6e5-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





