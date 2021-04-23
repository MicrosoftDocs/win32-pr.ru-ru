---
title: Сообщение HDM_GETITEMDROPDOWNRECT (Коммктрл. h)
description: Возвращает ограничивающий прямоугольник кнопки разворачивающегося элемента заголовка со стилем ХДФ \_ SPLITBUTTON. Отправляйте это сообщение явным образом или с помощью \_ макроса Жетитемдропдовнрект заголовка.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Элементы управления Windows для HDM_GETITEMDROPDOWNRECT сообщений
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071656"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="ebcf7-105">\_Сообщение ЖЕТИТЕМДРОПДОВНРЕКТ HDM</span><span class="sxs-lookup"><span data-stu-id="ebcf7-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="ebcf7-106">Возвращает ограничивающий прямоугольник кнопки разворачивающегося элемента заголовка со стилем **ХДФ \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="ebcf7-107">Отправляйте это сообщение явным образом или с помощью макроса [**\_ жетитемдропдовнрект заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .</span><span class="sxs-lookup"><span data-stu-id="ebcf7-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebcf7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebcf7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebcf7-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebcf7-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcf7-110">Отсчитываемый от нуля индекс элемента управления заголовка, для которого требуется получить ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ebcf7-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ebcf7-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcf7-112">Указатель на структуру [**Rect**](/windows/win32/api/windef/ns-windef-rect) , которая получает сведения об ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="ebcf7-113">Отправитель сообщения отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="ebcf7-114">Координаты, возвращаемые в структуре RECT, выражаются относительно родительского элемента управления заголовка.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebcf7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebcf7-115">Return value</span></span>

<span data-ttu-id="ebcf7-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebcf7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ebcf7-117">Remarks</span></span>

<span data-ttu-id="ebcf7-118">Элемент заголовка должен иметь Style **ХДФ \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="ebcf7-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebcf7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ebcf7-119">Requirements</span></span>



| <span data-ttu-id="ebcf7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ebcf7-120">Requirement</span></span> | <span data-ttu-id="ebcf7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ebcf7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebcf7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebcf7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebcf7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ebcf7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebcf7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebcf7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebcf7-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ebcf7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebcf7-126">Header</span><span class="sxs-lookup"><span data-stu-id="ebcf7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebcf7-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebcf7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebcf7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebcf7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebcf7-129">Сведения об элементах управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="ebcf7-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





