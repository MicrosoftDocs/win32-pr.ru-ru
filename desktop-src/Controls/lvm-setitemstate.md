---
title: Сообщение LVM_SETITEMSTATE (Коммктрл. h)
description: Изменяет состояние элемента в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетитемстате ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- Элементы управления Windows для LVM_SETITEMSTATE сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136062"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="e2dac-105">\_Сообщение LVM сетитемстате</span><span class="sxs-lookup"><span data-stu-id="e2dac-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="e2dac-106">Изменяет состояние элемента в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="e2dac-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="e2dac-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетитемстате ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .</span><span class="sxs-lookup"><span data-stu-id="e2dac-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2dac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2dac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2dac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2dac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2dac-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="e2dac-110">Index of the list-view item.</span></span> <span data-ttu-id="e2dac-111">Если этот параметр имеет значение-1, то изменение состояния применяется ко всем элементам.</span><span class="sxs-lookup"><span data-stu-id="e2dac-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="e2dac-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2dac-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2dac-113">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="e2dac-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="e2dac-114">Элемент **статемаск** указывает, какие биты состояния следует изменить, а элемент **State** содержит новые значения для этих битов.</span><span class="sxs-lookup"><span data-stu-id="e2dac-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="e2dac-115">Остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="e2dac-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2dac-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2dac-116">Return value</span></span>

<span data-ttu-id="e2dac-117">Если сообщение отправляется явным образом, оно возвращает **true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e2dac-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2dac-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2dac-118">Remarks</span></span>

<span data-ttu-id="e2dac-119">Значение состояния элемента включает набор битовых флагов, указывающих на состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e2dac-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="e2dac-120">Значение состояния может также включать индексы списка изображений, указывающие изображение состояния элемента и изображение оверлея.</span><span class="sxs-lookup"><span data-stu-id="e2dac-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2dac-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e2dac-121">Requirements</span></span>



| <span data-ttu-id="e2dac-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e2dac-122">Requirement</span></span> | <span data-ttu-id="e2dac-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e2dac-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dac-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2dac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2dac-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2dac-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2dac-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2dac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2dac-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2dac-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2dac-128">Header</span><span class="sxs-lookup"><span data-stu-id="e2dac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2dac-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2dac-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





