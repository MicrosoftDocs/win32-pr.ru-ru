---
title: Сообщение LVM_INSERTGROUP (Коммктрл. h)
description: Вставляет группу в элемент управления "представление списка".
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- Элементы управления Windows для LVM_INSERTGROUP сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654646"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="b869a-104">\_Сообщение LVM инсертграуп</span><span class="sxs-lookup"><span data-stu-id="b869a-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="b869a-105">Вставляет группу в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="b869a-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b869a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b869a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b869a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b869a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b869a-108">Индекс, по которому добавляется группа.</span><span class="sxs-lookup"><span data-stu-id="b869a-108">Index where the group is to be added.</span></span> <span data-ttu-id="b869a-109">Если это значение равно-1, группа добавляется в конец списка.</span><span class="sxs-lookup"><span data-stu-id="b869a-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="b869a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b869a-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b869a-111">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**лвграуп**</a> , содержащую добавляемую группу.</span><span class="sxs-lookup"><span data-stu-id="b869a-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b869a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b869a-112">Return value</span></span>

<span data-ttu-id="b869a-113">Возвращает индекс элемента, к которому была добавлена группа, или значение-1, если операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b869a-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b869a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b869a-114">Remarks</span></span>

<span data-ttu-id="b869a-115">Чтобы включить режим группы, вызовите [**LVM \_ Енаблеграупвиев**](lvm-enablegroupview.md) или [**ListView \_ енаблеграупвиев**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span><span class="sxs-lookup"><span data-stu-id="b869a-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="b869a-116">Невозможно вставить группу в пустой элемент управления "список-представление".</span><span class="sxs-lookup"><span data-stu-id="b869a-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="b869a-117">Не забудьте задать **играупид** в элементах, в которые была добавлена группа.</span><span class="sxs-lookup"><span data-stu-id="b869a-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="b869a-118">В противном случае после обработки сообщения [**LVM \_ енаблеграупвиев**](lvm-enablegroupview.md) со значением **true** элемент управления ListView не будет отображать ни одного элемента.</span><span class="sxs-lookup"><span data-stu-id="b869a-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="b869a-119">Чтобы использовать это сообщение, необходимо предоставить манифест с указанием Comclt32 версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="b869a-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="b869a-120">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b869a-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b869a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b869a-121">Requirements</span></span>



| <span data-ttu-id="b869a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b869a-122">Requirement</span></span> | <span data-ttu-id="b869a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b869a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b869a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b869a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b869a-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b869a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b869a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b869a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b869a-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b869a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b869a-128">Header</span><span class="sxs-lookup"><span data-stu-id="b869a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b869a-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b869a-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





