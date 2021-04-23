---
title: Сообщение TVM_SORTCHILDREN (Коммктрл. h)
description: Сортирует дочерние элементы указанного родительского элемента в элементе управления иерархического представления. Это сообщение можно отправить явно или с помощью \_ макроса Сортчилдрен TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Элементы управления Windows для TVM_SORTCHILDREN сообщений
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071957"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="09731-105">\_Сообщение TVM сортчилдрен</span><span class="sxs-lookup"><span data-stu-id="09731-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="09731-106">Сортирует дочерние элементы указанного родительского элемента в элементе управления иерархического представления.</span><span class="sxs-lookup"><span data-stu-id="09731-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="09731-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сортчилдрен TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .</span><span class="sxs-lookup"><span data-stu-id="09731-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="09731-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="09731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09731-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09731-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09731-110">Значение, указывающее, является ли сортировка рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="09731-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="09731-111">Присвойте параметру *wParam* **значение true** , чтобы сортировать все уровни дочерних элементов под родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="09731-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="09731-112">В противном случае сортируются только непосредственные дочерние элементы родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="09731-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="09731-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09731-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09731-114">Обработчик родительского элемента, дочерние элементы которого должны быть отсортированы.</span><span class="sxs-lookup"><span data-stu-id="09731-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09731-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09731-115">Return value</span></span>

<span data-ttu-id="09731-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="09731-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="09731-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09731-117">Remarks</span></span>

<span data-ttu-id="09731-118">Это сообщение алфабетизес элементы дерева с помощью [**лстркмпи**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) в имени элемента.</span><span class="sxs-lookup"><span data-stu-id="09731-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="09731-119">Чтобы настроить поведение при упорядочении, можно использовать сообщение [**TVM \_ сортчилдренкб**](tvm-sortchildrencb.md) .</span><span class="sxs-lookup"><span data-stu-id="09731-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="09731-120">Требования</span><span class="sxs-lookup"><span data-stu-id="09731-120">Requirements</span></span>



| <span data-ttu-id="09731-121">Требование</span><span class="sxs-lookup"><span data-stu-id="09731-121">Requirement</span></span> | <span data-ttu-id="09731-122">Значение</span><span class="sxs-lookup"><span data-stu-id="09731-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09731-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09731-123">Minimum supported client</span></span><br/> | <span data-ttu-id="09731-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09731-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09731-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09731-125">Minimum supported server</span></span><br/> | <span data-ttu-id="09731-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09731-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09731-127">Header</span><span class="sxs-lookup"><span data-stu-id="09731-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="09731-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="09731-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

