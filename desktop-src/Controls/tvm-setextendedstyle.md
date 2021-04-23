---
title: Сообщение TVM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Информирует элемент управления представлением дерева о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос TreeView \_ сетекстендедстиле.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Элементы управления Windows для TVM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534343"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="a80da-105">\_Сообщение TVM сетекстендедстиле</span><span class="sxs-lookup"><span data-stu-id="a80da-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="a80da-106">Информирует элемент управления представлением дерева о необходимости установки расширенных стилей.</span><span class="sxs-lookup"><span data-stu-id="a80da-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="a80da-107">Отправьте это сообщение или используйте макрос [**TreeView \_ сетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="a80da-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="a80da-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a80da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80da-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a80da-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a80da-110">Маска, используемая для выбора устанавливаемых стилей.</span><span class="sxs-lookup"><span data-stu-id="a80da-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="a80da-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a80da-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a80da-112">Значение, указывающее расширенный стиль.</span><span class="sxs-lookup"><span data-stu-id="a80da-112">Value that indicates the extended style.</span></span> <span data-ttu-id="a80da-113">Дополнительные сведения о стилях см. в разделе [Расширенные стили элемента управления "дерево-представление](tree-view-control-window-extended-styles.md)".</span><span class="sxs-lookup"><span data-stu-id="a80da-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80da-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a80da-114">Return value</span></span>

<span data-ttu-id="a80da-115">Если это сообщение завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a80da-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a80da-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a80da-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80da-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a80da-117">Remarks</span></span>

<span data-ttu-id="a80da-118">Расширенные стили для элемента управления "дерево" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="a80da-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="a80da-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a80da-119">Requirements</span></span>



| <span data-ttu-id="a80da-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a80da-120">Requirement</span></span> | <span data-ttu-id="a80da-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a80da-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a80da-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a80da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a80da-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a80da-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a80da-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a80da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a80da-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a80da-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a80da-126">Header</span><span class="sxs-lookup"><span data-stu-id="a80da-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80da-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80da-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

