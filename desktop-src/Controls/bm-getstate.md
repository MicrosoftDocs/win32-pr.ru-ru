---
title: Сообщение BM_GETSTATE (Winuser. h)
description: Получает состояние кнопки или флажка. Это сообщение можно отправить явным образом или воспользоваться макросом "Кнопка" \_ .
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Элементы управления Windows для BM_GETSTATE сообщений
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988248"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="29801-105">Сообщение BM о \_ состоянии</span><span class="sxs-lookup"><span data-stu-id="29801-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="29801-106">Получает состояние кнопки или флажка.</span><span class="sxs-lookup"><span data-stu-id="29801-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="29801-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**"Кнопка" \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .</span><span class="sxs-lookup"><span data-stu-id="29801-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="29801-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="29801-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29801-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29801-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29801-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="29801-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="29801-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29801-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29801-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="29801-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29801-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29801-113">Return value</span></span>

<span data-ttu-id="29801-114">Возвращаемое значение указывает текущее состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="29801-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="29801-115">Это сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="29801-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="29801-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="29801-116">Return code</span></span>                                                                                        | <span data-ttu-id="29801-117">Описание</span><span class="sxs-lookup"><span data-stu-id="29801-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29801-118"><dt>**\_установлен флажок BST**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="29801-119">Кнопка отмечена флажком.</span><span class="sxs-lookup"><span data-stu-id="29801-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="29801-120"><dt>**\_ДРОПДОВНПУШЕД BST**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="29801-121">[Windows Vista](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="29801-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="29801-122">Кнопка находится в раскрывающемся состоянии.</span><span class="sxs-lookup"><span data-stu-id="29801-122">The button is in the drop-down state.</span></span> <span data-ttu-id="29801-123">Применяется только в том случае, если кнопка имеет стиль [**\_ раскрывающегося списка тбстиле**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="29801-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="29801-124"><dt>**\_фокус BST**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="29801-125">Кнопка имеет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="29801-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="29801-126"><dt>**горячий в BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="29801-127">Кнопка является активной; Это значит, что указатель мыши наведен на него.</span><span class="sxs-lookup"><span data-stu-id="29801-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="29801-128"><dt>**BST не \_ определено**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="29801-129">Состояние кнопки является неопределенным.</span><span class="sxs-lookup"><span data-stu-id="29801-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="29801-130">Применяется только в том случае, если кнопка имеет стиль [**BS \_ 3STATE**](button-styles.md) или [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="29801-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="29801-131"><dt>**помещается в BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="29801-132">Кнопка отображается в состоянии отправлено.</span><span class="sxs-lookup"><span data-stu-id="29801-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="29801-133"><dt>**не \_ отмечено в BST**</dt></span><span class="sxs-lookup"><span data-stu-id="29801-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="29801-134">Нет специального состояния.</span><span class="sxs-lookup"><span data-stu-id="29801-134">No special state.</span></span> <span data-ttu-id="29801-135">Эквивалентно нулю.</span><span class="sxs-lookup"><span data-stu-id="29801-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="29801-136">Требования</span><span class="sxs-lookup"><span data-stu-id="29801-136">Requirements</span></span>



| <span data-ttu-id="29801-137">Требование</span><span class="sxs-lookup"><span data-stu-id="29801-137">Requirement</span></span> | <span data-ttu-id="29801-138">Значение</span><span class="sxs-lookup"><span data-stu-id="29801-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29801-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29801-139">Minimum supported client</span></span><br/> | <span data-ttu-id="29801-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29801-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="29801-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29801-141">Minimum supported server</span></span><br/> | <span data-ttu-id="29801-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29801-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29801-143">Header</span><span class="sxs-lookup"><span data-stu-id="29801-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="29801-144"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29801-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29801-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29801-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="29801-146">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="29801-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29801-147">**BM \_**</span><span class="sxs-lookup"><span data-stu-id="29801-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="29801-148">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="29801-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





