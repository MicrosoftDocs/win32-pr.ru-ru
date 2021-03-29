---
title: Сообщение LVM_GETITEMINDEXRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для всей или части подэлемента в текущем представлении элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетитеминдексрект ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Элементы управления Windows для LVM_GETITEMINDEXRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492414"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="95f60-105">\_Сообщение LVM жетитеминдексрект</span><span class="sxs-lookup"><span data-stu-id="95f60-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="95f60-106">Извлекает ограничивающий прямоугольник для всей или части подэлемента в текущем представлении элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="95f60-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="95f60-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетитеминдексрект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .</span><span class="sxs-lookup"><span data-stu-id="95f60-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95f60-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95f60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f60-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95f60-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f60-110">Указатель на структуру [**лвитеминдекс**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) для родительского элемента подэлемента.</span><span class="sxs-lookup"><span data-stu-id="95f60-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="95f60-111">Вызывающий процесс отвечает за выделение этой структуры и задание ее членов.</span><span class="sxs-lookup"><span data-stu-id="95f60-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="95f60-112">*wParam* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="95f60-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95f60-113">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="95f60-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95f60-114">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения координат.</span><span class="sxs-lookup"><span data-stu-id="95f60-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="95f60-115">Вызывающий процесс отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="95f60-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="95f60-116">Значение *lParam* не должно быть **null**.</span><span class="sxs-lookup"><span data-stu-id="95f60-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="95f60-117">Установите **верхний** элемент в качестве индекса подэлемента.</span><span class="sxs-lookup"><span data-stu-id="95f60-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="95f60-118">Установите для **левого** элемента одно из следующих значений, указывающее часть подэлемента, для которой должен быть получен ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="95f60-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="95f60-119">Значение</span><span class="sxs-lookup"><span data-stu-id="95f60-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="95f60-120">Значение</span><span class="sxs-lookup"><span data-stu-id="95f60-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="95f60-121"><dt>**\_границы лвир**</dt></span><span class="sxs-lookup"><span data-stu-id="95f60-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="95f60-122">Возвращает ограничивающий прямоугольник для всего вложенного элемента, включая значок и метку.</span><span class="sxs-lookup"><span data-stu-id="95f60-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="95f60-123"><dt>**\_значок лвир**</dt></span><span class="sxs-lookup"><span data-stu-id="95f60-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="95f60-124">Возвращает ограничивающий прямоугольник значка или маленький значок подэлемента.</span><span class="sxs-lookup"><span data-stu-id="95f60-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="95f60-125"><dt>**\_Метка лвир**</dt></span><span class="sxs-lookup"><span data-stu-id="95f60-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="95f60-126">Возвращает ограничивающий прямоугольник для текста подэлемента.</span><span class="sxs-lookup"><span data-stu-id="95f60-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f60-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95f60-127">Return value</span></span>

<span data-ttu-id="95f60-128">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="95f60-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f60-129">Требования</span><span class="sxs-lookup"><span data-stu-id="95f60-129">Requirements</span></span>



| <span data-ttu-id="95f60-130">Требование</span><span class="sxs-lookup"><span data-stu-id="95f60-130">Requirement</span></span> | <span data-ttu-id="95f60-131">Значение</span><span class="sxs-lookup"><span data-stu-id="95f60-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95f60-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95f60-132">Minimum supported client</span></span><br/> | <span data-ttu-id="95f60-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95f60-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95f60-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95f60-134">Minimum supported server</span></span><br/> | <span data-ttu-id="95f60-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95f60-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95f60-136">Header</span><span class="sxs-lookup"><span data-stu-id="95f60-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="95f60-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="95f60-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

