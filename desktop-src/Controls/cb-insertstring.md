---
title: Сообщение CB_INSERTSTRING (Winuser. h)
description: Вставляет строку или данные элемента в список поля со списком. В отличие от \_ сообщения ADDSTRING CB, \_ сообщение инсертстринг CB не приводит к сортировке списка с использованием \_ стиля сортировки CBS.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Элементы управления Windows для CB_INSERTSTRING сообщений
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490542"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="d47c7-105">\_Сообщение ИНСЕРТСТРИНГ CB</span><span class="sxs-lookup"><span data-stu-id="d47c7-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="d47c7-106">Вставляет строку или данные элемента в список поля со списком.</span><span class="sxs-lookup"><span data-stu-id="d47c7-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="d47c7-107">В отличие от [**сообщения \_ ADDSTRING CB**](cb-addstring.md) , сообщение **\_ инсертстринг CB** не приводит к сортировке списка с использованием [**стиля \_ сортировки CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d47c7-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="d47c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d47c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47c7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d47c7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d47c7-110">Отсчитываемый от нуля индекс позиции, в которую вставляется строка.</span><span class="sxs-lookup"><span data-stu-id="d47c7-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="d47c7-111">Если этот параметр имеет значение-1, строка добавляется в конец списка.</span><span class="sxs-lookup"><span data-stu-id="d47c7-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="d47c7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d47c7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d47c7-113">Указатель на вставляемую строку, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="d47c7-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="d47c7-114">Если создать поле со списком с помощью стиля, рисуемого владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , то значение параметра *lParam* сохраняется, а не строка, в которую он мог бы в противном случае указать.</span><span class="sxs-lookup"><span data-stu-id="d47c7-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d47c7-115">Return value</span></span>

<span data-ttu-id="d47c7-116">Возвращаемое значение — это индекс позиции, в которую была вставлена строка.</span><span class="sxs-lookup"><span data-stu-id="d47c7-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="d47c7-117">Если возникает ошибка, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d47c7-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="d47c7-118">Если недостаточно места для хранения новой строки, это будет \_ ЕРРСПАЦЕ CB.</span><span class="sxs-lookup"><span data-stu-id="d47c7-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="d47c7-119">Если поле со списком имеет [**стиль \_ HSCROLL**](/windows/desktop/winmsg/window-styles) и вы вставляете строку шире, чем поле со списком, следует отправить сообщение [**\_ сесоризонталекстент фунтов**](lb-sethorizontalextent.md) , чтобы появилась горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d47c7-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47c7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d47c7-120">Requirements</span></span>



| <span data-ttu-id="d47c7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d47c7-121">Requirement</span></span> | <span data-ttu-id="d47c7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d47c7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47c7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d47c7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d47c7-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d47c7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d47c7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d47c7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d47c7-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d47c7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d47c7-127">Header</span><span class="sxs-lookup"><span data-stu-id="d47c7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d47c7-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d47c7-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47c7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d47c7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d47c7-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d47c7-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d47c7-131">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="d47c7-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="d47c7-132">**сесоризонталекстент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="d47c7-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="d47c7-133">**\_Каталог CB**</span><span class="sxs-lookup"><span data-stu-id="d47c7-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 

