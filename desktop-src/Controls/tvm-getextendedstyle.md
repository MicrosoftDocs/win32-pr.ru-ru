---
title: Сообщение TVM_GETEXTENDEDSTYLE (Коммктрл. h)
description: Возвращает расширенный стиль для элемента управления "дерево-представление". Отправьте это сообщение явно или с помощью \_ макроса Жетекстендедстиле TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Элементы управления Windows для TVM_GETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892605"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="e7557-105">Сообщение TVM_GETEXTENDEDSTYLE (Коммктрл. h)</span><span class="sxs-lookup"><span data-stu-id="e7557-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="e7557-106">Возвращает расширенный стиль для элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="e7557-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="e7557-107">Отправьте это сообщение явно или с помощью макроса [**\_ жетекстендедстиле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="e7557-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7557-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7557-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7557-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7557-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7557-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e7557-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7557-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7557-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e7557-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e7557-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7557-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7557-113">Return value</span></span>

<span data-ttu-id="e7557-114">Возвращает значение расширенного стиля. Дополнительные сведения о стилях см. в разделе [Расширенные стили элемента управления "дерево-представление](tree-view-control-window-extended-styles.md)".</span><span class="sxs-lookup"><span data-stu-id="e7557-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7557-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7557-115">Remarks</span></span>

<span data-ttu-id="e7557-116">Расширенные стили для элемента управления "дерево" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="e7557-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7557-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e7557-117">Requirements</span></span>



| <span data-ttu-id="e7557-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e7557-118">Requirement</span></span> | <span data-ttu-id="e7557-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e7557-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7557-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7557-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7557-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7557-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7557-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7557-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7557-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7557-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7557-124">Header</span><span class="sxs-lookup"><span data-stu-id="e7557-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7557-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7557-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

