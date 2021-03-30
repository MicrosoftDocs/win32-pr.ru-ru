---
title: Сообщение TVM_MAPACCIDTOHTREEITEM (Коммктрл. h)
description: Сопоставляет идентификатор доступа с ХТРИИТЕМ.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Элементы управления Windows для TVM_MAPACCIDTOHTREEITEM сообщений
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071362"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="3cfad-104">\_Сообщение TVM мапакЦидтохтриитем</span><span class="sxs-lookup"><span data-stu-id="3cfad-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="3cfad-105">Сопоставляет идентификатор доступа с **хтриитем**.</span><span class="sxs-lookup"><span data-stu-id="3cfad-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cfad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cfad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cfad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cfad-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3cfad-108">**Uint** , содержащий идентификатор доступа, сопоставляемый с **хтриитем**.</span><span class="sxs-lookup"><span data-stu-id="3cfad-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="3cfad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cfad-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3cfad-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3cfad-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cfad-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cfad-111">Return value</span></span>

<span data-ttu-id="3cfad-112">Возвращает **хтриитем** , с которым СОПОСТАВЛЕН указанный идентификатор доступа.</span><span class="sxs-lookup"><span data-stu-id="3cfad-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cfad-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cfad-113">Remarks</span></span>

<span data-ttu-id="3cfad-114">При добавлении элемента в элемент управления представлением в виде дерева возвращается **хтриитем** , который однозначно определяет элемент.</span><span class="sxs-lookup"><span data-stu-id="3cfad-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="3cfad-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3cfad-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="3cfad-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfad-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3cfad-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3cfad-117">Requirements</span></span>



| <span data-ttu-id="3cfad-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3cfad-118">Requirement</span></span> | <span data-ttu-id="3cfad-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3cfad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfad-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cfad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfad-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3cfad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cfad-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cfad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfad-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3cfad-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cfad-124">Header</span><span class="sxs-lookup"><span data-stu-id="3cfad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cfad-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cfad-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cfad-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cfad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cfad-127">**\_МапакЦидтохтриитем TreeView**</span><span class="sxs-lookup"><span data-stu-id="3cfad-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





