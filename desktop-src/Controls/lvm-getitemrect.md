---
title: Сообщение LVM_GETITEMRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для всего элемента или его части в текущем представлении. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемрект ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Элементы управления Windows для LVM_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071906"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="12d71-105">\_Сообщение LVM жетитемрект</span><span class="sxs-lookup"><span data-stu-id="12d71-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="12d71-106">Извлекает ограничивающий прямоугольник для всего элемента или его части в текущем представлении.</span><span class="sxs-lookup"><span data-stu-id="12d71-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="12d71-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемрект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="12d71-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="12d71-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12d71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d71-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12d71-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d71-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="12d71-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="12d71-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="12d71-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12d71-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="12d71-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="12d71-113">При отправке сообщения **левый** элемент этой структуры используется для указания части элемента списка, из которой извлекается ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="12d71-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="12d71-114">Необходимо задать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="12d71-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="12d71-115">Значение</span><span class="sxs-lookup"><span data-stu-id="12d71-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="12d71-116">Значение</span><span class="sxs-lookup"><span data-stu-id="12d71-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="12d71-117"><dt>**\_границы лвир**</dt></span><span class="sxs-lookup"><span data-stu-id="12d71-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="12d71-118">Возвращает ограничивающий прямоугольник для всего элемента, включая значок и метку.</span><span class="sxs-lookup"><span data-stu-id="12d71-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="12d71-119"><dt>**\_значок лвир**</dt></span><span class="sxs-lookup"><span data-stu-id="12d71-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="12d71-120">Возвращает ограничивающий прямоугольник значка или маленький значок.</span><span class="sxs-lookup"><span data-stu-id="12d71-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="12d71-121"><dt>**\_Метка лвир**</dt></span><span class="sxs-lookup"><span data-stu-id="12d71-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="12d71-122">Возвращает ограничивающий прямоугольник текста элемента.</span><span class="sxs-lookup"><span data-stu-id="12d71-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="12d71-123"><dt>**ЛВИР \_ селектбаундс**</dt></span><span class="sxs-lookup"><span data-stu-id="12d71-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="12d71-124">Возвращает объединение ЛВИР \_ значка и \_ прямоугольников меток лвир, но исключает столбцы в представлении отчета.</span><span class="sxs-lookup"><span data-stu-id="12d71-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d71-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12d71-125">Return value</span></span>

<span data-ttu-id="12d71-126">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="12d71-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d71-127">Требования</span><span class="sxs-lookup"><span data-stu-id="12d71-127">Requirements</span></span>



| <span data-ttu-id="12d71-128">Требование</span><span class="sxs-lookup"><span data-stu-id="12d71-128">Requirement</span></span> | <span data-ttu-id="12d71-129">Значение</span><span class="sxs-lookup"><span data-stu-id="12d71-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12d71-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12d71-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12d71-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12d71-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12d71-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12d71-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12d71-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12d71-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12d71-134">Header</span><span class="sxs-lookup"><span data-stu-id="12d71-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d71-135"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d71-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

