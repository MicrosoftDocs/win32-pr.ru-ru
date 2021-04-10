---
title: Код уведомления TVN_ENDLABELEDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления об окончании редактирования метки для элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136046"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="83ab4-105">\_Код уведомления ТВН ендлабеледит</span><span class="sxs-lookup"><span data-stu-id="83ab4-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="83ab4-106">Сообщает родительскому окну элемента управления иерархического представления об окончании редактирования метки для элемента.</span><span class="sxs-lookup"><span data-stu-id="83ab4-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="83ab4-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="83ab4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="83ab4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83ab4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ab4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83ab4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83ab4-110">Указатель на структуру [**нмтвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="83ab4-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="83ab4-111">**Элемент** этой структуры является структурой [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , члены которой **хитем**, **lParam** и **псзтекст** содержат действительные сведения об элементе, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="83ab4-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="83ab4-112">Если изменение метки было отменено, элемент **псзтекст** структуры **Твитем** имеет **значение NULL**. в противном случае **псзтекст** является адресом редактируемого текста.</span><span class="sxs-lookup"><span data-stu-id="83ab4-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ab4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83ab4-113">Return value</span></span>

<span data-ttu-id="83ab4-114">Если элемент **псзтекст** имеет значение, отличное от **null**, возвращает **значение true** , чтобы задать метку элемента для редактируемого текста.</span><span class="sxs-lookup"><span data-stu-id="83ab4-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="83ab4-115">Возвращает **значение false** , чтобы отклонить измененный текст и вернуться к исходной метке.</span><span class="sxs-lookup"><span data-stu-id="83ab4-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ab4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83ab4-116">Remarks</span></span>

<span data-ttu-id="83ab4-117">Если элемент **псзтекст** имеет **значение NULL**, возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="83ab4-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="83ab4-118">Если \_ для этого элемента задано значение LPSTR тексткаллбакк, а элемент **псзтекст** не равен **null**, \_ обработчик ТВН ендлабеледит должен скопировать текст из **псзтекст** в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="83ab4-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ab4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="83ab4-119">Requirements</span></span>



| <span data-ttu-id="83ab4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="83ab4-120">Requirement</span></span> | <span data-ttu-id="83ab4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="83ab4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83ab4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83ab4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="83ab4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83ab4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83ab4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83ab4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="83ab4-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83ab4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83ab4-126">Header</span><span class="sxs-lookup"><span data-stu-id="83ab4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="83ab4-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="83ab4-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="83ab4-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="83ab4-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83ab4-129">**ТВН \_ ЕНДЛАБЕЛЕДИТВ** (Юникод) и **ТВН \_ ендлабеледита** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="83ab4-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





