---
title: Сообщение LVM_GETSUBITEMRECT (Коммктрл. h)
description: Извлекает сведения о ограничивающем прямоугольнике для подэлемента в элементе управления "представление списка".
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Элементы управления Windows для LVM_GETSUBITEMRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137106"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="1664e-104">\_Сообщение LVM жетсубитемрект</span><span class="sxs-lookup"><span data-stu-id="1664e-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="1664e-105">Извлекает сведения о ограничивающем прямоугольнике для подэлемента в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="1664e-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="1664e-106">Это сообщение можно отправить явно или с помощью макроса [**\_ жетсубитемрект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="1664e-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="1664e-107">Это сообщение предназначено для использования только с элементами управления "представление списка", которые используют стиль [**\_ отчета LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1664e-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="1664e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1664e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1664e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1664e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1664e-110">Индекс родительского элемента подэлемента.</span><span class="sxs-lookup"><span data-stu-id="1664e-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="1664e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1664e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1664e-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получит сведения о ограничивающем прямоугольнике для подэлемента.</span><span class="sxs-lookup"><span data-stu-id="1664e-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="1664e-113">Его члены должны быть инициализированы в соответствии со следующими связями "член-значение":</span><span class="sxs-lookup"><span data-stu-id="1664e-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="1664e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1664e-114">Value</span></span>                                                                                                                             | <span data-ttu-id="1664e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1664e-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="1664e-116"><dt>**Вверх**</dt></span><span class="sxs-lookup"><span data-stu-id="1664e-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="1664e-117">Отсчитываемый от единицы индекс подэлемента.</span><span class="sxs-lookup"><span data-stu-id="1664e-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="1664e-118"><dt>**слева**</dt></span><span class="sxs-lookup"><span data-stu-id="1664e-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="1664e-119">Значение флага (см. примечания).</span><span class="sxs-lookup"><span data-stu-id="1664e-119">Flag value (see remarks).</span></span> <span data-ttu-id="1664e-120">Указывает часть подэлемента представления списка, для которой необходимо получить ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="1664e-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1664e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1664e-121">Return value</span></span>

<span data-ttu-id="1664e-122">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1664e-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1664e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1664e-123">Remarks</span></span>

<span data-ttu-id="1664e-124">Ниже приведены значения флагов, которые могут быть установлены.</span><span class="sxs-lookup"><span data-stu-id="1664e-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="1664e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1664e-125">Requirement</span></span> | <span data-ttu-id="1664e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1664e-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1664e-127">**Значение флага**</span><span class="sxs-lookup"><span data-stu-id="1664e-127">**Flag Value**</span></span> | <span data-ttu-id="1664e-128">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1664e-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="1664e-129">\_границы лвир</span><span class="sxs-lookup"><span data-stu-id="1664e-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="1664e-130">Возвращает ограничивающий прямоугольник для всего элемента, включая значок и метку.</span><span class="sxs-lookup"><span data-stu-id="1664e-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="1664e-131">\_значок лвир</span><span class="sxs-lookup"><span data-stu-id="1664e-131">LVIR\_ICON</span></span>     | <span data-ttu-id="1664e-132">Возвращает ограничивающий прямоугольник значка или маленький значок.</span><span class="sxs-lookup"><span data-stu-id="1664e-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="1664e-133">\_Метка лвир</span><span class="sxs-lookup"><span data-stu-id="1664e-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="1664e-134">Возвращает ограничивающий прямоугольник для всего элемента, включая значок и метку.</span><span class="sxs-lookup"><span data-stu-id="1664e-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="1664e-135">Это аналогично \_ границам лвир.</span><span class="sxs-lookup"><span data-stu-id="1664e-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1664e-136">Требования</span><span class="sxs-lookup"><span data-stu-id="1664e-136">Requirements</span></span>



| <span data-ttu-id="1664e-137">Требование</span><span class="sxs-lookup"><span data-stu-id="1664e-137">Requirement</span></span> | <span data-ttu-id="1664e-138">Значение</span><span class="sxs-lookup"><span data-stu-id="1664e-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1664e-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1664e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1664e-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1664e-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1664e-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1664e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1664e-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1664e-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1664e-143">Header</span><span class="sxs-lookup"><span data-stu-id="1664e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1664e-144"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1664e-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

