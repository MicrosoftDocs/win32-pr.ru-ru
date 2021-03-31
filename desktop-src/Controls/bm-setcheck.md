---
title: Сообщение BM_SETCHECK (Winuser. h)
description: Задает состояние флажка для переключателя или флажка. Это сообщение можно отправить явно или с помощью \_ макроса кнопки сетчекк.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Элементы управления Windows для BM_SETCHECK сообщений
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071204"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="867d1-105">\_Сообщение BM сетчекк</span><span class="sxs-lookup"><span data-stu-id="867d1-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="867d1-106">Задает состояние флажка для переключателя или флажка.</span><span class="sxs-lookup"><span data-stu-id="867d1-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="867d1-107">Это сообщение можно отправить явно или с помощью макроса [**кнопки \_ сетчекк**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .</span><span class="sxs-lookup"><span data-stu-id="867d1-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="867d1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="867d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="867d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="867d1-110">Состояние проверки.</span><span class="sxs-lookup"><span data-stu-id="867d1-110">The check state.</span></span> <span data-ttu-id="867d1-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="867d1-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="867d1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="867d1-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="867d1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="867d1-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="867d1-114"><dt>**\_установлен флажок BST**</dt></span><span class="sxs-lookup"><span data-stu-id="867d1-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="867d1-115">Устанавливает состояние кнопки "установлен".</span><span class="sxs-lookup"><span data-stu-id="867d1-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="867d1-116"><dt>**BST не \_ определено**</dt></span><span class="sxs-lookup"><span data-stu-id="867d1-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="867d1-117">Устанавливает состояние кнопки серым цветом, указывая на неопределенное состояние.</span><span class="sxs-lookup"><span data-stu-id="867d1-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="867d1-118">Используйте это значение только в том случае, если у кнопки есть стиль [**\_ 3STATE**](button-styles.md) или [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="867d1-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="867d1-119"><dt>**не \_ отмечено в BST**</dt></span><span class="sxs-lookup"><span data-stu-id="867d1-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="867d1-120">Задает состояние кнопки "Очистка".</span><span class="sxs-lookup"><span data-stu-id="867d1-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="867d1-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="867d1-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="867d1-122">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="867d1-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="867d1-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="867d1-123">Return value</span></span>

<span data-ttu-id="867d1-124">Это сообщение всегда возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="867d1-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="867d1-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="867d1-125">Remarks</span></span>

<span data-ttu-id="867d1-126">Сообщение **BM \_ сетчекк** не влияет на кнопки Push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="867d1-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="867d1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="867d1-127">Requirements</span></span>



| <span data-ttu-id="867d1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="867d1-128">Requirement</span></span> | <span data-ttu-id="867d1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="867d1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="867d1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="867d1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="867d1-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="867d1-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="867d1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="867d1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="867d1-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="867d1-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="867d1-134">Header</span><span class="sxs-lookup"><span data-stu-id="867d1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="867d1-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="867d1-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867d1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="867d1-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="867d1-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="867d1-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="867d1-138">**BM \_**</span><span class="sxs-lookup"><span data-stu-id="867d1-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="867d1-139">**BM \_**</span><span class="sxs-lookup"><span data-stu-id="867d1-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="867d1-140">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="867d1-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





