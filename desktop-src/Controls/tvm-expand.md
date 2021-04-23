---
title: Сообщение TVM_EXPAND (Коммктрл. h)
description: Сообщение TVM \_ Expand разворачивает или сворачивает список дочерних элементов, связанных с указанным родительским элементом, если таковой имеется. Это сообщение можно отправить явно или с помощью \_ макроса развертывания TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Элементы управления Windows для TVM_EXPAND сообщений
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492378"
---
# <a name="tvm_expand-message"></a><span data-ttu-id="7fe33-105">TVM \_ развернуть сообщение</span><span class="sxs-lookup"><span data-stu-id="7fe33-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="7fe33-106">Сообщение **TVM \_ expand** разворачивает или сворачивает список дочерних элементов, связанных с указанным родительским элементом, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="7fe33-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="7fe33-107">Это сообщение можно отправить явно или с помощью макроса [**\_ развертывания TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .</span><span class="sxs-lookup"><span data-stu-id="7fe33-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fe33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fe33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fe33-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fe33-110">Флаг действия.</span><span class="sxs-lookup"><span data-stu-id="7fe33-110">Action flag.</span></span> <span data-ttu-id="7fe33-111">Этот параметр может принимать одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7fe33-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="7fe33-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7fe33-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="7fe33-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7fe33-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="7fe33-114"><dt>**ТВЕ \_ Свернуть**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe33-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="7fe33-115">Сворачивает список.</span><span class="sxs-lookup"><span data-stu-id="7fe33-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="7fe33-116"><dt>**ТВЕ \_ коллапсересет**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe33-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="7fe33-117">Сворачивает список и удаляет дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="7fe33-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="7fe33-118">Флаг состояния [**ТВИС \_ експандедонце**](tree-view-control-item-states.md) сброшен.</span><span class="sxs-lookup"><span data-stu-id="7fe33-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="7fe33-119">Этот флаг должен использоваться с \_ флагом СВОРАЧИВАНИЯ тве.</span><span class="sxs-lookup"><span data-stu-id="7fe33-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="7fe33-120"><dt>**\_развернуть тве**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe33-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="7fe33-121">Раскрывает список.</span><span class="sxs-lookup"><span data-stu-id="7fe33-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="7fe33-122"><dt>**ТВЕ \_ експандпартиал**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe33-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="7fe33-123">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7fe33-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="7fe33-124">Частично расширяет список.</span><span class="sxs-lookup"><span data-stu-id="7fe33-124">Partially expands the list.</span></span> <span data-ttu-id="7fe33-125">В этом состоянии дочерние элементы видимы и знак плюс (+) родительского элемента, указывающий, что он может быть развернут, отображается.</span><span class="sxs-lookup"><span data-stu-id="7fe33-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="7fe33-126">Этот флаг следует использовать в сочетании с \_ флагом развертывания тве.</span><span class="sxs-lookup"><span data-stu-id="7fe33-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="7fe33-127"><dt>**\_переключатель тве**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe33-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="7fe33-128">Сворачивает список, если он развернут, или разворачивает его, если он свернут.</span><span class="sxs-lookup"><span data-stu-id="7fe33-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="7fe33-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fe33-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fe33-130">Обработчик родительского элемента, который необходимо развернуть или свернуть.</span><span class="sxs-lookup"><span data-stu-id="7fe33-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe33-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fe33-131">Return value</span></span>

<span data-ttu-id="7fe33-132">Возвращает ненулевое значение, если операция выполнена успешно, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7fe33-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fe33-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fe33-133">Remarks</span></span>

<span data-ttu-id="7fe33-134">Расширение уже развернутого узла считается успешной операцией, и [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7fe33-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="7fe33-135">Свертывание узла возвращает нуль, если узел уже свернут; в противном случае возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7fe33-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="7fe33-136">Попытка развернуть или свернуть узел, не имеющий дочерних элементов, считается ошибкой, а **SendMessage** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7fe33-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="7fe33-137">Когда элемент сначала разворачивается с помощью **сообщения \_ TVM Expand** , действие создает коды уведомлений [ТВН \_ итемекспандинг](tvn-itemexpanding.md) и [ТВН \_ итемекспандед](tvn-itemexpanded.md) , а также установлен флаг элемента [**ТВИС \_ експандедонце**](tree-view-control-item-states.md) State.</span><span class="sxs-lookup"><span data-stu-id="7fe33-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="7fe33-138">Если этот флаг состояния остается установленным, последующие сообщения **TVM \_ expand** не создают \_ уведомления ТВН итемекспандинг или ТВН \_ итемекспандед.</span><span class="sxs-lookup"><span data-stu-id="7fe33-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="7fe33-139">Чтобы сбросить флаг состояния **ТВИС \_ експандедонце** , необходимо отправить TVM-сообщение **\_ расширения** с \_ \_ установленными флагами тве свернуть и тве коллапсересет.</span><span class="sxs-lookup"><span data-stu-id="7fe33-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="7fe33-140">Попытка явного задания **ТВИС \_ експандедонце** приведет к непредсказуемому поведению.</span><span class="sxs-lookup"><span data-stu-id="7fe33-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="7fe33-141">Операция развертывания может завершиться ошибкой, если владелец элемента управления TreeView отклоняет операцию в ответ на уведомление [ТВН \_ итемекспандинг](tvn-itemexpanding.md) .</span><span class="sxs-lookup"><span data-stu-id="7fe33-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe33-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7fe33-142">Requirements</span></span>



| <span data-ttu-id="7fe33-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7fe33-143">Requirement</span></span> | <span data-ttu-id="7fe33-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7fe33-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe33-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fe33-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe33-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fe33-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fe33-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fe33-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe33-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fe33-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fe33-149">Header</span><span class="sxs-lookup"><span data-stu-id="7fe33-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe33-150"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe33-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

