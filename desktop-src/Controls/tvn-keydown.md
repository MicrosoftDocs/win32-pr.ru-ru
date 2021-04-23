---
title: Код уведомления TVN_KEYDOWN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что пользователь нажал на клавишу, а элемент управления "представление дерева" имеет фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489015"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="995b9-105">\_Код уведомления ТВН KeyDown</span><span class="sxs-lookup"><span data-stu-id="995b9-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="995b9-106">Сообщает родительскому окну элемента управления древовидного представления о том, что пользователь нажал на клавишу, а элемент управления "представление дерева" имеет фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="995b9-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="995b9-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="995b9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="995b9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="995b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="995b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="995b9-110">Указатель на структуру [**нмтвкэйдовн**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="995b9-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="995b9-111">Элемент **ввкэй** указывает виртуальный код ключа.</span><span class="sxs-lookup"><span data-stu-id="995b9-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995b9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="995b9-112">Return value</span></span>

<span data-ttu-id="995b9-113">Если **ввкэй** членом *lParam* является символьный код клавиши, он будет использоваться в процессе добавочного поиска.</span><span class="sxs-lookup"><span data-stu-id="995b9-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="995b9-114">Возвращает ненулевое значение, чтобы исключить символ из последовательного поиска, или нуль, чтобы включить символ в поиск.</span><span class="sxs-lookup"><span data-stu-id="995b9-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="995b9-115">Для всех остальных ключей возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="995b9-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="995b9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="995b9-116">Requirements</span></span>



| <span data-ttu-id="995b9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="995b9-117">Requirement</span></span> | <span data-ttu-id="995b9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="995b9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="995b9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="995b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="995b9-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="995b9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="995b9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="995b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="995b9-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="995b9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="995b9-123">Header</span><span class="sxs-lookup"><span data-stu-id="995b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="995b9-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="995b9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





