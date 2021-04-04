---
title: Сообщение CB_ADDSTRING (Winuser. h)
description: Добавляет строку в список поля со списком. Если поле со списком не имеет \_ стиля сортировки CBS, строка добавляется в конец списка. В противном случае строка вставляется в список, а список сортируется.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Элементы управления Windows для CB_ADDSTRING сообщений
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989196"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="71a5e-106">\_Сообщение ADDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="71a5e-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="71a5e-107">Добавляет строку в список поля со списком.</span><span class="sxs-lookup"><span data-stu-id="71a5e-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="71a5e-108">Если поле со списком не имеет стиля [**\_ сортировки CBS**](combo-box-styles.md) , строка добавляется в конец списка.</span><span class="sxs-lookup"><span data-stu-id="71a5e-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="71a5e-109">В противном случае строка вставляется в список, а список сортируется.</span><span class="sxs-lookup"><span data-stu-id="71a5e-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="71a5e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="71a5e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71a5e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71a5e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71a5e-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="71a5e-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="71a5e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71a5e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71a5e-114">Указатель **LPCTSTR** на добавляемую строку, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="71a5e-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="71a5e-115">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , значение параметра *lParam* сохраняется как данные элемента, а не как строка, на которую он мог бы в противном случае указать.</span><span class="sxs-lookup"><span data-stu-id="71a5e-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="71a5e-116">Данные элемента можно получить или изменить, отправив сообщение [**CB \_ Жетитемдата**](cb-getitemdata.md) или [**CB \_ сетитемдата**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="71a5e-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71a5e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71a5e-117">Return value</span></span>

<span data-ttu-id="71a5e-118">Возвращаемое значение — это Отсчитываемый от нуля индекс строки в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="71a5e-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="71a5e-119">Если возникает ошибка, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="71a5e-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="71a5e-120">Если недостаточно места для хранения новой строки, это будет \_ ЕРРСПАЦЕ CB.</span><span class="sxs-lookup"><span data-stu-id="71a5e-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="71a5e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71a5e-121">Remarks</span></span>

<span data-ttu-id="71a5e-122">При создании поля со списком, рисуемого владельцем, с использованием стиля [**\_ сортировки CBS**](combo-box-styles.md) , но без стиля [**\_ хасстрингс**](combo-box-styles.md) , сообщение [**WM \_ компареитем**](wm-compareitem.md) отправляется владельцу поля со списком один или несколько раз, чтобы новый элемент можно было правильно поместить в список.</span><span class="sxs-lookup"><span data-stu-id="71a5e-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="71a5e-123">Чтобы вставить строку в определенное место в списке, используйте сообщение [**\_ инсертстринг CB**](cb-insertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="71a5e-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="71a5e-124">Если поле со списком имеет стиль [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) и вы добавляете строку шире, чем поле со списком, отправьте [**сообщение \_ сесоризонталекстент фунтов**](lb-sethorizontalextent.md) , чтобы появилась горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="71a5e-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="71a5e-125">**Comclt32.dll версии 5,0 или более поздней:** Если заданы [**\_ строчные**](combo-box-styles.md) или [**CBS \_**](combo-box-styles.md) в нижнем регистре, версия в Юникоде **\_ ADDSTRING** изменяет строку.</span><span class="sxs-lookup"><span data-stu-id="71a5e-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="71a5e-126">Если используется глобальная память только для чтения, это приводит к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="71a5e-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a5e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="71a5e-127">Requirements</span></span>



| <span data-ttu-id="71a5e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="71a5e-128">Requirement</span></span> | <span data-ttu-id="71a5e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="71a5e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a5e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71a5e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="71a5e-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71a5e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71a5e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71a5e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="71a5e-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71a5e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71a5e-134">Header</span><span class="sxs-lookup"><span data-stu-id="71a5e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="71a5e-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71a5e-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a5e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71a5e-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="71a5e-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="71a5e-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71a5e-138">**\_Каталог CB**</span><span class="sxs-lookup"><span data-stu-id="71a5e-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="71a5e-139">**\_ИНСЕРТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="71a5e-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="71a5e-140">**сесоризонталекстент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="71a5e-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="71a5e-141">**WM \_ компареитем**</span><span class="sxs-lookup"><span data-stu-id="71a5e-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

