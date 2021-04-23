---
title: Сообщение TVM_GETCOUNT (Коммктрл. h)
description: Извлекает число элементов в элементе управления "дерево". Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Элементы управления Windows для TVM_GETCOUNT сообщений
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492372"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="dac9b-105">TVM \_ ВЫчислить сообщение</span><span class="sxs-lookup"><span data-stu-id="dac9b-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="dac9b-106">Извлекает число элементов в элементе управления "дерево".</span><span class="sxs-lookup"><span data-stu-id="dac9b-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="dac9b-107">Это сообщение можно отправить явным образом или с помощью макроса [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .</span><span class="sxs-lookup"><span data-stu-id="dac9b-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dac9b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dac9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac9b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dac9b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dac9b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dac9b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dac9b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dac9b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dac9b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dac9b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac9b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dac9b-113">Return value</span></span>

<span data-ttu-id="dac9b-114">Возвращает число элементов.</span><span class="sxs-lookup"><span data-stu-id="dac9b-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac9b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dac9b-115">Remarks</span></span>

<span data-ttu-id="dac9b-116">Число узлов, возвращенное [**TreeView- \_ Count**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) , ограничено целыми значениями.</span><span class="sxs-lookup"><span data-stu-id="dac9b-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="dac9b-117">При добавлении узла за пределами 32767 макрос возвращает отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="dac9b-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="dac9b-118">После добавления 65536 узлов счетчик возвращается к нулю.</span><span class="sxs-lookup"><span data-stu-id="dac9b-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="dac9b-119">В этом случае элемент управления "представление дерева" отображается как пустой без полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="dac9b-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac9b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dac9b-120">Requirements</span></span>



| <span data-ttu-id="dac9b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dac9b-121">Requirement</span></span> | <span data-ttu-id="dac9b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dac9b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dac9b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dac9b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dac9b-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dac9b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dac9b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dac9b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dac9b-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dac9b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dac9b-127">Header</span><span class="sxs-lookup"><span data-stu-id="dac9b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac9b-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac9b-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





