---
title: Сообщение TVM_SHOWINFOTIP (Коммктрл. h)
description: Отображает всплывающую подсказку для указанного элемента в элементе управления "представление дерева". Это сообщение можно отправить явно или с помощью \_ макроса Шовинфотип TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Элементы управления Windows для TVM_SHOWINFOTIP сообщений
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892714"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="3aeaa-105">\_Сообщение TVM шовинфотип</span><span class="sxs-lookup"><span data-stu-id="3aeaa-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="3aeaa-106">Отображает всплывающую подсказку для указанного элемента в элементе управления "представление дерева".</span><span class="sxs-lookup"><span data-stu-id="3aeaa-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="3aeaa-107">Это сообщение можно отправить явно или с помощью макроса [**\_ шовинфотип TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .</span><span class="sxs-lookup"><span data-stu-id="3aeaa-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="3aeaa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3aeaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aeaa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3aeaa-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3aeaa-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3aeaa-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3aeaa-111">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3aeaa-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aeaa-112">Маркер для элемента.</span><span class="sxs-lookup"><span data-stu-id="3aeaa-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aeaa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3aeaa-113">Return value</span></span>

<span data-ttu-id="3aeaa-114">Возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3aeaa-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aeaa-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3aeaa-115">Remarks</span></span>

<span data-ttu-id="3aeaa-116">Большинство приложений не используют это сообщение.</span><span class="sxs-lookup"><span data-stu-id="3aeaa-116">Most applications do not use this message.</span></span> <span data-ttu-id="3aeaa-117">Инфотипс отображаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="3aeaa-117">Infotips are shown automatically.</span></span> <span data-ttu-id="3aeaa-118">Дополнительные сведения см. в разделе Использование Инфотипс в представлении "Общие сведения [об элементах управления Tree-View](tree-view-controls.md) ".</span><span class="sxs-lookup"><span data-stu-id="3aeaa-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aeaa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3aeaa-119">Requirements</span></span>



| <span data-ttu-id="3aeaa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3aeaa-120">Requirement</span></span> | <span data-ttu-id="3aeaa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3aeaa-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3aeaa-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3aeaa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3aeaa-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3aeaa-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3aeaa-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3aeaa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3aeaa-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3aeaa-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3aeaa-126">Header</span><span class="sxs-lookup"><span data-stu-id="3aeaa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aeaa-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aeaa-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





