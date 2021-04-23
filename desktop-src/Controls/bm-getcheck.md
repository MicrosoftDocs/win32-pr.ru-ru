---
title: Сообщение BM_GETCHECK (Winuser. h)
description: Возвращает состояние флажка для переключателя или флажка. Это сообщение можно отправить явным образом или с помощью макроса с кнопкой "выполнить \_ проверку".
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Элементы управления Windows для BM_GETCHECK сообщений
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137291"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="78c3c-105">Сообщение BM о \_ проверке</span><span class="sxs-lookup"><span data-stu-id="78c3c-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="78c3c-106">Возвращает состояние флажка для переключателя или флажка.</span><span class="sxs-lookup"><span data-stu-id="78c3c-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="78c3c-107">Это сообщение можно отправить явным образом или с помощью макроса с [**кнопкой "выполнить \_ проверку"**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .</span><span class="sxs-lookup"><span data-stu-id="78c3c-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="78c3c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="78c3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c3c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78c3c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78c3c-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="78c3c-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="78c3c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78c3c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78c3c-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="78c3c-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c3c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78c3c-113">Return value</span></span>

<span data-ttu-id="78c3c-114">Возвращаемое значение из кнопки, созданной с [**помощью \_ автофлажка BS**](button-styles.md), " [**\_ автоradiobutton**](button-styles.md)", "BS [**\_ AUTO3STATE**](button-styles.md) [**", \_ "флажок BS", "BS" или "**](button-styles.md) [**BS \_ 3STATE**](button-styles.md) " [**, может \_**](button-styles.md)быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="78c3c-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="78c3c-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="78c3c-115">Return code</span></span>                                                                                       | <span data-ttu-id="78c3c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="78c3c-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78c3c-117"><dt>**\_установлен флажок BST**</dt></span><span class="sxs-lookup"><span data-stu-id="78c3c-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="78c3c-118">Флажок установлен.</span><span class="sxs-lookup"><span data-stu-id="78c3c-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="78c3c-119"><dt>**BST не \_ определено**</dt></span><span class="sxs-lookup"><span data-stu-id="78c3c-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="78c3c-120">Отображается серым цветом, что означает неопределенное состояние (применяется только в том случае, если кнопка имеет стиль [**\_ 3STATE**](button-styles.md) или [**BS \_ AUTO3STATE**](button-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="78c3c-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="78c3c-121"><dt>**не \_ отмечено в BST**</dt></span><span class="sxs-lookup"><span data-stu-id="78c3c-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="78c3c-122">Кнопка сброшена</span><span class="sxs-lookup"><span data-stu-id="78c3c-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="78c3c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78c3c-123">Remarks</span></span>

<span data-ttu-id="78c3c-124">Если у кнопки есть стиль, отличный от перечисленных, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="78c3c-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c3c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="78c3c-125">Requirements</span></span>



| <span data-ttu-id="78c3c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="78c3c-126">Requirement</span></span> | <span data-ttu-id="78c3c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="78c3c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c3c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78c3c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="78c3c-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78c3c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78c3c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78c3c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="78c3c-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78c3c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78c3c-132">Header</span><span class="sxs-lookup"><span data-stu-id="78c3c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="78c3c-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78c3c-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c3c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78c3c-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="78c3c-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="78c3c-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78c3c-136">**BM \_**</span><span class="sxs-lookup"><span data-stu-id="78c3c-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="78c3c-137">**BM \_ сетчекк**</span><span class="sxs-lookup"><span data-stu-id="78c3c-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





