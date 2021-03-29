---
title: Сообщение LVM_GETGROUPRECT (Коммктрл. h)
description: Возвращает прямоугольник для указанной группы. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупрект ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Элементы управления Windows для LVM_GETGROUPRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988240"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="696c7-105">\_Сообщение LVM жетграупрект</span><span class="sxs-lookup"><span data-stu-id="696c7-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="696c7-106">Возвращает прямоугольник для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="696c7-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="696c7-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетграупрект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .</span><span class="sxs-lookup"><span data-stu-id="696c7-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="696c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="696c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="696c7-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="696c7-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="696c7-110">Задает Group By **играупид** (см. структуру [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="696c7-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="696c7-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="696c7-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="696c7-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения сведений о группе, заданной параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="696c7-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="696c7-113">Получатель сообщений отвечает за присвоение членам структуры сведений о группе, заданной параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="696c7-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="696c7-114">Вызывающий процесс отвечает за выделение памяти для структуры.</span><span class="sxs-lookup"><span data-stu-id="696c7-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="696c7-115">Установите в качестве **верхнего** элемента [**Rect**](/previous-versions//dd162897(v=vs.85)) один из следующих флагов, чтобы указать координаты получаемого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="696c7-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="696c7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="696c7-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="696c7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="696c7-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="696c7-118"><dt>**\_Группа лвггр**</dt></span><span class="sxs-lookup"><span data-stu-id="696c7-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="696c7-119">Координаты всей развернутой группы.</span><span class="sxs-lookup"><span data-stu-id="696c7-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="696c7-120"><dt>**\_заголовок лвггр**</dt></span><span class="sxs-lookup"><span data-stu-id="696c7-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="696c7-121">Координаты только заголовка (свернутая группа).</span><span class="sxs-lookup"><span data-stu-id="696c7-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="696c7-122"><dt>**\_Метка лвггр**</dt></span><span class="sxs-lookup"><span data-stu-id="696c7-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="696c7-123">Координаты только метки.</span><span class="sxs-lookup"><span data-stu-id="696c7-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="696c7-124"><dt>**ЛВГГР \_ субсетлинк**</dt></span><span class="sxs-lookup"><span data-stu-id="696c7-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="696c7-125">Координаты только ссылки на подмножество (подмножество разметки).</span><span class="sxs-lookup"><span data-stu-id="696c7-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="696c7-126">Элемент управления "представление списка" может ограничивать количество видимых элементов, отображаемых в каждой группе.</span><span class="sxs-lookup"><span data-stu-id="696c7-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="696c7-127">Для пользователя предоставляется ссылка, позволяющая пользователю развернуть группу.</span><span class="sxs-lookup"><span data-stu-id="696c7-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="696c7-128">Этот флаг Возвращает ограничивающий прямоугольник ссылки на подмножество, если группа является подмножеством (состояние группы ЛВГС "подмножество \_ ", см. раздел Structure [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **состояние** элемента).</span><span class="sxs-lookup"><span data-stu-id="696c7-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="696c7-129">Этот флаг предоставляется, чтобы приложения со специальными возможностями могли найти ссылку.</span><span class="sxs-lookup"><span data-stu-id="696c7-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="696c7-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="696c7-130">Return value</span></span>

<span data-ttu-id="696c7-131">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="696c7-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="696c7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="696c7-132">Requirements</span></span>



| <span data-ttu-id="696c7-133">Требование</span><span class="sxs-lookup"><span data-stu-id="696c7-133">Requirement</span></span> | <span data-ttu-id="696c7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="696c7-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="696c7-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="696c7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="696c7-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="696c7-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="696c7-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="696c7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="696c7-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="696c7-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="696c7-139">Header</span><span class="sxs-lookup"><span data-stu-id="696c7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="696c7-140"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="696c7-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

