---
title: Сообщение TVM_MAPHTREEITEMTOACCID (Коммктрл. h)
description: Сопоставляет ХТРИИТЕМ с ИДЕНТИФИКАТОРом специальных возможностей.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Элементы управления Windows для TVM_MAPHTREEITEMTOACCID сообщений
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135926"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="76bb4-104">\_Сообщение TVM мафтриитемтоакЦид</span><span class="sxs-lookup"><span data-stu-id="76bb4-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="76bb4-105">Сопоставляет **хтриитем** с идентификатором специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="76bb4-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="76bb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76bb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76bb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76bb4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76bb4-108">**Хтриитем** , сопоставленный с идентификатором специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="76bb4-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="76bb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76bb4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76bb4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="76bb4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76bb4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76bb4-111">Return value</span></span>

<span data-ttu-id="76bb4-112">Возвращает идентификатор специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="76bb4-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="76bb4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76bb4-113">Remarks</span></span>

<span data-ttu-id="76bb4-114">При добавлении элемента в элемент управления "дерево" возвращается маркер **хтриитем** , который однозначно определяет элемент.</span><span class="sxs-lookup"><span data-stu-id="76bb4-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="76bb4-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="76bb4-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="76bb4-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76bb4-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76bb4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="76bb4-117">Requirements</span></span>



| <span data-ttu-id="76bb4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="76bb4-118">Requirement</span></span> | <span data-ttu-id="76bb4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="76bb4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76bb4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76bb4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76bb4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76bb4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76bb4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76bb4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76bb4-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76bb4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76bb4-124">Header</span><span class="sxs-lookup"><span data-stu-id="76bb4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76bb4-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="76bb4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76bb4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76bb4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76bb4-127">**\_МафтриитемтоакЦид TreeView**</span><span class="sxs-lookup"><span data-stu-id="76bb4-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





