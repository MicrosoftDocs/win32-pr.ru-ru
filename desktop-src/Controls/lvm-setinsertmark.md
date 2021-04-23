---
title: Сообщение LVM_SETINSERTMARK (Коммктрл. h)
description: Задает точку вставки в заданную позицию.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Элементы управления Windows для LVM_SETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135118"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="d9665-104">\_Сообщение LVM сетинсертмарк</span><span class="sxs-lookup"><span data-stu-id="d9665-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="d9665-105">Задает точку вставки в заданную позицию.</span><span class="sxs-lookup"><span data-stu-id="d9665-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9665-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9665-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9665-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d9665-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d9665-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d9665-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9665-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9665-110">Указатель на структуру <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">лвинсертмарк</a> , указывающую место установки точки вставки.</span><span class="sxs-lookup"><span data-stu-id="d9665-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9665-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9665-111">Return value</span></span>

<span data-ttu-id="d9665-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d9665-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="d9665-113">**Значение false** возвращается, если размер элемента **кбсизе** структуры [**лвинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) не равен фактическому размеру структуры или если точка вставки не применяется в текущем представлении.</span><span class="sxs-lookup"><span data-stu-id="d9665-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9665-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9665-114">Remarks</span></span>

<span data-ttu-id="d9665-115">Точка вставки может отображаться только в том случае, если элемент управления "представление списка" находится в представлении значков, представлении с небольшим значком или мозаичном представлении, а не в режиме просмотра группы.</span><span class="sxs-lookup"><span data-stu-id="d9665-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="d9665-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="d9665-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d9665-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9665-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9665-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d9665-118">Requirements</span></span>



| <span data-ttu-id="d9665-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d9665-119">Requirement</span></span> | <span data-ttu-id="d9665-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d9665-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9665-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9665-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9665-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9665-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9665-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9665-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9665-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9665-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9665-125">Header</span><span class="sxs-lookup"><span data-stu-id="d9665-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9665-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9665-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





