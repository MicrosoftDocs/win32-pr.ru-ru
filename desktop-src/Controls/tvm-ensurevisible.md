---
title: Сообщение TVM_ENSUREVISIBLE (Коммктрл. h)
description: Обеспечивает видимость элемента представления в виде дерева, расширяя родительский элемент или прокручивает элемент управления представлением дерева, если это необходимо. Это сообщение можно отправить явно или с помощью \_ макроса Енсуревисибле TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- Элементы управления Windows для TVM_ENSUREVISIBLE сообщений
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988468"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="289f2-105">\_Сообщение TVM енсуревисибле</span><span class="sxs-lookup"><span data-stu-id="289f2-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="289f2-106">Обеспечивает видимость элемента представления в виде дерева, расширяя родительский элемент или прокручивает элемент управления представлением дерева, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="289f2-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="289f2-107">Это сообщение можно отправить явно или с помощью макроса [**\_ енсуревисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="289f2-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="289f2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="289f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="289f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="289f2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="289f2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="289f2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="289f2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="289f2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="289f2-112">Маркер для элемента.</span><span class="sxs-lookup"><span data-stu-id="289f2-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="289f2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="289f2-113">Return value</span></span>

<span data-ttu-id="289f2-114">Возвращает ненулевое значение, если система прокручивает элементы в элементе управления "дерево" и никакие элементы не были развернуты.</span><span class="sxs-lookup"><span data-stu-id="289f2-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="289f2-115">В противном случае сообщение возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="289f2-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="289f2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="289f2-116">Remarks</span></span>

<span data-ttu-id="289f2-117">Если сообщение TVM \_ енсуревисибле расширяет родительский элемент, родительское окно получает коды уведомлений [ТВН \_ итемекспандинг](tvn-itemexpanding.md) и [ТВН \_ итемекспандед](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="289f2-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="289f2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="289f2-118">Requirements</span></span>



| <span data-ttu-id="289f2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="289f2-119">Requirement</span></span> | <span data-ttu-id="289f2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="289f2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="289f2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="289f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="289f2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="289f2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="289f2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="289f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="289f2-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="289f2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="289f2-125">Header</span><span class="sxs-lookup"><span data-stu-id="289f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="289f2-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="289f2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





