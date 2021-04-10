---
title: Сообщение LVM_ARRANGE (Коммктрл. h)
description: Упорядочивает элементы в представлении значков. Это сообщение можно отправить явно или с помощью \_ макроса компоновки ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Элементы управления Windows для LVM_ARRANGE сообщений
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135143"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="e2e37-105">LVM \_ Размещение сообщения</span><span class="sxs-lookup"><span data-stu-id="e2e37-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="e2e37-106">Упорядочивает элементы в представлении значков.</span><span class="sxs-lookup"><span data-stu-id="e2e37-106">Arranges items in icon view.</span></span> <span data-ttu-id="e2e37-107">Это сообщение можно отправить явно или с помощью макроса [**\_ компоновки ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .</span><span class="sxs-lookup"><span data-stu-id="e2e37-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2e37-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2e37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e37-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2e37-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2e37-110">Одно из следующих значений, определяющее выравнивание:</span><span class="sxs-lookup"><span data-stu-id="e2e37-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="e2e37-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e2e37-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="e2e37-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e2e37-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="e2e37-113"><dt>**ЛВА \_ алигнлефт**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e37-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="e2e37-114">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="e2e37-114">Not implemented.</span></span> <span data-ttu-id="e2e37-115">Примените вместо этого стиль [**LVS \_ алигнлефт**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e2e37-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="e2e37-116"><dt>**ЛВА \_ алигнтоп**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e37-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="e2e37-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="e2e37-117">Not implemented.</span></span> <span data-ttu-id="e2e37-118">Примените вместо этого стиль [**LVS \_ алигнтоп**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e2e37-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="e2e37-119"><dt>**ЛВА \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e37-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="e2e37-120">Выравнивает элементы в соответствии с текущими стилями выравнивания элемента управления представления списка (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e2e37-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="e2e37-121"><dt>**ЛВА \_ SNAPTOGRID**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e37-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="e2e37-122">Привязывает все значки к ближайшей положению сетки.</span><span class="sxs-lookup"><span data-stu-id="e2e37-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="e2e37-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2e37-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2e37-124">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e2e37-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e37-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2e37-125">Return value</span></span>

<span data-ttu-id="e2e37-126">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e2e37-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e37-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e2e37-127">Requirements</span></span>



| <span data-ttu-id="e2e37-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e2e37-128">Requirement</span></span> | <span data-ttu-id="e2e37-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e2e37-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e37-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2e37-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e37-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2e37-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2e37-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2e37-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e37-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2e37-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2e37-134">Header</span><span class="sxs-lookup"><span data-stu-id="e2e37-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e37-135"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e37-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





