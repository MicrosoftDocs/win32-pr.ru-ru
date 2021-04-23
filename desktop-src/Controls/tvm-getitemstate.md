---
title: Сообщение TVM_GETITEMSTATE (Коммктрл. h)
description: Извлекает некоторые или все атрибуты состояния элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемстате TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Элементы управления Windows для TVM_GETITEMSTATE сообщений
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071804"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="ee49c-105">\_Сообщение TVM жетитемстате</span><span class="sxs-lookup"><span data-stu-id="ee49c-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="ee49c-106">Извлекает некоторые или все атрибуты состояния элемента представления дерева.</span><span class="sxs-lookup"><span data-stu-id="ee49c-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="ee49c-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемстате TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="ee49c-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee49c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee49c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee49c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee49c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee49c-110">Маркер для элемента.</span><span class="sxs-lookup"><span data-stu-id="ee49c-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="ee49c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee49c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee49c-112">Маска, используемая для указания состояний для запроса.</span><span class="sxs-lookup"><span data-stu-id="ee49c-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="ee49c-113">Он эквивалентен элементу **статемаск** элемента [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="ee49c-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee49c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee49c-114">Return value</span></span>

<span data-ttu-id="ee49c-115">Возвращает значение **uint** с соответствующими битами состояния, установленным в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ee49c-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="ee49c-116">Будут установлены только те биты, которые указаны в параметре *lParam* и имеют **значение true** .</span><span class="sxs-lookup"><span data-stu-id="ee49c-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="ee49c-117">Это значение эквивалентно значению элемента **State** объекта [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="ee49c-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee49c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ee49c-118">Requirements</span></span>



| <span data-ttu-id="ee49c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ee49c-119">Requirement</span></span> | <span data-ttu-id="ee49c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ee49c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee49c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee49c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee49c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee49c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee49c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee49c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee49c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee49c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee49c-125">Header</span><span class="sxs-lookup"><span data-stu-id="ee49c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee49c-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee49c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





