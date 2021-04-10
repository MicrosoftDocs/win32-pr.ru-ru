---
title: Сообщение TVM_SETINDENT (Коммктрл. h)
description: Задает ширину отступа для элемента управления "представление в виде дерева" и перерисовывает элемент управления для отражения новой ширины. Это сообщение можно отправить явно или с помощью \_ макроса Сетиндент TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Элементы управления Windows для TVM_SETINDENT сообщений
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136231"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="87f36-105">\_Сообщение TVM сетиндент</span><span class="sxs-lookup"><span data-stu-id="87f36-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="87f36-106">Задает ширину отступа для элемента управления "представление в виде дерева" и перерисовывает элемент управления для отражения новой ширины.</span><span class="sxs-lookup"><span data-stu-id="87f36-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="87f36-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетиндент TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .</span><span class="sxs-lookup"><span data-stu-id="87f36-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="87f36-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="87f36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f36-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87f36-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f36-110">Ширина (в пикселях) отступа.</span><span class="sxs-lookup"><span data-stu-id="87f36-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="87f36-111">Если этот параметр меньше, чем определенная системой минимальная ширина, то для новой ширины задается минимум, определенный системой.</span><span class="sxs-lookup"><span data-stu-id="87f36-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="87f36-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87f36-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87f36-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="87f36-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f36-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87f36-114">Return value</span></span>

<span data-ttu-id="87f36-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="87f36-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f36-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87f36-116">Remarks</span></span>

<span data-ttu-id="87f36-117">Определенное системой минимальное значение отступа обычно составляет пять пикселей, но не фиксировано.</span><span class="sxs-lookup"><span data-stu-id="87f36-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="87f36-118">Чтобы получить точное значение минимального отступа в определенной системе, отправьте сообщение **TVM \_ сетиндент** с параметром *wParam* , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="87f36-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="87f36-119">Затем отправьте сообщение [**TVM с \_ отступом**](tvm-getindent.md) , чтобы получить минимальное значение отступа.</span><span class="sxs-lookup"><span data-stu-id="87f36-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f36-120">Требования</span><span class="sxs-lookup"><span data-stu-id="87f36-120">Requirements</span></span>



| <span data-ttu-id="87f36-121">Требование</span><span class="sxs-lookup"><span data-stu-id="87f36-121">Requirement</span></span> | <span data-ttu-id="87f36-122">Значение</span><span class="sxs-lookup"><span data-stu-id="87f36-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87f36-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87f36-123">Minimum supported client</span></span><br/> | <span data-ttu-id="87f36-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87f36-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87f36-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87f36-125">Minimum supported server</span></span><br/> | <span data-ttu-id="87f36-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87f36-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87f36-127">Header</span><span class="sxs-lookup"><span data-stu-id="87f36-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f36-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f36-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f36-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87f36-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f36-130">**\_Сетиндент TreeView**</span><span class="sxs-lookup"><span data-stu-id="87f36-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





