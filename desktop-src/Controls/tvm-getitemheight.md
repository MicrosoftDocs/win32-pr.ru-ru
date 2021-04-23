---
title: Сообщение TVM_GETITEMHEIGHT (Коммктрл. h)
description: Извлекает текущую высоту каждого элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса GetItemHeight TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Элементы управления Windows для TVM_GETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892786"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="b6586-105">\_Сообщение TVM GETITEMHEIGHT</span><span class="sxs-lookup"><span data-stu-id="b6586-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="b6586-106">Извлекает текущую высоту каждого элемента представления дерева.</span><span class="sxs-lookup"><span data-stu-id="b6586-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="b6586-107">Это сообщение можно отправить явно или с помощью макроса [**\_ GetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .</span><span class="sxs-lookup"><span data-stu-id="b6586-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6586-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6586-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6586-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6586-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b6586-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b6586-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b6586-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6586-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b6586-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b6586-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6586-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6586-113">Return value</span></span>

<span data-ttu-id="b6586-114">Возвращает высоту каждого элемента в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b6586-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6586-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b6586-115">Requirements</span></span>



| <span data-ttu-id="b6586-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b6586-116">Requirement</span></span> | <span data-ttu-id="b6586-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b6586-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6586-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6586-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6586-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6586-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6586-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6586-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6586-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6586-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6586-122">Header</span><span class="sxs-lookup"><span data-stu-id="b6586-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6586-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6586-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6586-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6586-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6586-125">**TVM \_ сетитемхеигхт**</span><span class="sxs-lookup"><span data-stu-id="b6586-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





