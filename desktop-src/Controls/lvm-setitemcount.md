---
title: Сообщение LVM_SETITEMCOUNT (Коммктрл. h)
description: Заставляет элемент управления "представление списка" выделить память для указанного числа элементов или задать виртуальное количество элементов в элементе управления виртуального представления списка.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- Элементы управления Windows для LVM_SETITEMCOUNT сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135462"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="b4a2b-104">\_Сообщение LVM сетитемкаунт</span><span class="sxs-lookup"><span data-stu-id="b4a2b-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="b4a2b-105">Заставляет элемент управления "представление списка" выделить память для указанного числа элементов или задать виртуальное количество элементов в [элементе управления виртуального представления списка](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b4a2b-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="b4a2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4a2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a2b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4a2b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a2b-108">Число элементов, которые в конечном итоге будет содержать элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="b4a2b-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="b4a2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4a2b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a2b-110">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b4a2b-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="b4a2b-111">Значения, определяющие поведение элемента управления "представление списка" после сброса числа элементов.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="b4a2b-112">Это значение может быть сочетанием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b4a2b-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="b4a2b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b4a2b-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="b4a2b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b4a2b-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="b4a2b-115"><dt>**ЛВСИКФ \_ ноинвалидатеалл**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a2b-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="b4a2b-116">Элемент управления "представление списка" не будет перерисовываться, если только затронутые элементы в настоящее время не доступны для просмотра.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="b4a2b-117"><dt>**ЛВСИКФ \_ ПРОкрутка**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a2b-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="b4a2b-118">Элемент управления "представление списка" не изменит позицию прокрутки при изменении числа элементов.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a2b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4a2b-119">Return value</span></span>

<span data-ttu-id="b4a2b-120">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a2b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4a2b-121">Remarks</span></span>

<span data-ttu-id="b4a2b-122">Распределение памяти зависит от способа создания элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="b4a2b-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="b4a2b-123">Это сообщение можно отправить явным образом или использовать макросы [**ListView \_ Сетитемкаунт**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) или [**ListView \_ сетитемкаунтекс**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .</span><span class="sxs-lookup"><span data-stu-id="b4a2b-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="b4a2b-124">Дополнительные сведения см. в статье [стиль виртуальных List-View](/windows/desktop/Controls/list-view-controls-overview).</span><span class="sxs-lookup"><span data-stu-id="b4a2b-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="b4a2b-125">Если элемент управления "список" был создан без стиля [**LVS \_ овнердата**](list-view-window-styles.md) , отправка этого сообщения приводит к выделению элементом управления внутренних структур данных для указанного числа элементов.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="b4a2b-126">Это не позволяет элементу управления распределять структуры данных при каждом добавлении элемента.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="b4a2b-127">Если элемент управления "представление списка" был создан с использованием стиля [**LVS \_ овнердата**](list-view-window-styles.md) (виртуального представления списка), то при отправке этого сообщения задается виртуальное количество элементов, содержащихся в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="b4a2b-128">Параметр *lParam* предназначен только для элементов управления "представление списка", использующих стили [**LVS \_ овнердата**](list-view-window-styles.md) и [**LVS \_ отчета**](list-view-window-styles.md) или [**LVS \_ списка**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a2b-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="b4a2b-129">Если представление "список общих элементов управления" является виртуализированным представлением списка ([**LVS \_ овнердата**](list-view-window-styles.md)), то в списке отображается ограничение в 100 000 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="b4a2b-130">В этом сценарии **LVM \_ сетитемкаунт** возвращает значение false, если оно имеет *wParam* 100 000 001.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a2b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b4a2b-131">Requirements</span></span>



| <span data-ttu-id="b4a2b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b4a2b-132">Requirement</span></span> | <span data-ttu-id="b4a2b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b4a2b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a2b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4a2b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a2b-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4a2b-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4a2b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4a2b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a2b-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4a2b-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4a2b-138">Header</span><span class="sxs-lookup"><span data-stu-id="b4a2b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4a2b-139"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a2b-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

