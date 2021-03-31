---
title: Сообщение LB_ADDSTRING (Winuser. h)
description: Добавляет строку в список. Если поле со списком не имеет \_ стиля сортировки фунтов, строка добавляется в конец списка. В противном случае строка вставляется в список, и список сортируется.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Элементы управления Windows для LB_ADDSTRING сообщений
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071557"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="5a5db-106">Сообщение ADDSTRING балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="5a5db-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="5a5db-107">Добавляет строку в список.</span><span class="sxs-lookup"><span data-stu-id="5a5db-107">Adds a string to a list box.</span></span> <span data-ttu-id="5a5db-108">Если поле со списком не имеет стиля [**\_ сортировки фунтов**](list-box-styles.md) , строка добавляется в конец списка.</span><span class="sxs-lookup"><span data-stu-id="5a5db-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="5a5db-109">В противном случае строка вставляется в список, и список сортируется.</span><span class="sxs-lookup"><span data-stu-id="5a5db-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a5db-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a5db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a5db-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a5db-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a5db-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="5a5db-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a5db-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a5db-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a5db-114">Указатель на строку, завершающуюся нулем, которую необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="5a5db-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="5a5db-115">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , этот параметр сохраняется как данные элемента, а не как строка.</span><span class="sxs-lookup"><span data-stu-id="5a5db-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="5a5db-116">Вы можете отправить сообщения **\_ жетитемдата** и **\_ сетитемдата** балансировки нагрузки для получения или изменения данных элемента.</span><span class="sxs-lookup"><span data-stu-id="5a5db-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a5db-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a5db-117">Return value</span></span>

<span data-ttu-id="5a5db-118">Возвращаемое значение — это Отсчитываемый от нуля индекс строки в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="5a5db-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="5a5db-119">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="5a5db-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="5a5db-120">Если недостаточно места для хранения новой строки, возвращается значение фунтов \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="5a5db-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a5db-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a5db-121">Remarks</span></span>

<span data-ttu-id="5a5db-122">Если список имеет стиль, рисуемый владельцем, и стиль [**\_ сортировки фунтов**](list-box-styles.md) , но не Хасстрингс в стиле [**фунта \_**](list-box-styles.md) , система отправляет сообщение [**WM \_ компареитем**](wm-compareitem.md) один или несколько раз владельцу окна списка для правильного размещения нового элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="5a5db-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="5a5db-123">Сообщение [**\_ инитстораже балансировки нагрузки**](lb-initstorage.md) помогает ускорить инициализацию списков с большим количеством элементов (более 100).</span><span class="sxs-lookup"><span data-stu-id="5a5db-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="5a5db-124">Он резервирует указанный объем памяти, чтобы последующие сообщения **\_ ADDSTRINGи балансировки нагрузки** занимали кратчайшее время.</span><span class="sxs-lookup"><span data-stu-id="5a5db-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="5a5db-125">Для параметров *wParam* и *lParam* можно использовать оценки.</span><span class="sxs-lookup"><span data-stu-id="5a5db-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="5a5db-126">При чрезмерной оценке выделяется дополнительный объем памяти. Если недооценивать, то для элементов, превышающих запрошенный объем, используется нормальное выделение.</span><span class="sxs-lookup"><span data-stu-id="5a5db-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="5a5db-127">Если список имеет стиль [**\_ HSCROLL**](/windows/desktop/winmsg/window-styles) и строка шире, чем поле списка, отправьте сообщение [**\_ сесоризонталекстент балансировки нагрузки**](lb-sethorizontalextent.md) , чтобы убедиться, что отображается горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="5a5db-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="5a5db-128">Для приложения ANSI система преобразует текст в поле со списком в Юникод с помощью команды CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="5a5db-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="5a5db-129">Это может вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="5a5db-129">This can cause problems.</span></span> <span data-ttu-id="5a5db-130">Например, римские символы с диакритическими знаками в списке не в Юникоде в японских окнах будут выступать из искажений.</span><span class="sxs-lookup"><span data-stu-id="5a5db-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="5a5db-131">Чтобы устранить эту проблему, либо скомпилируйте приложение как Юникод, либо используйте список, рисуемый владельцем.</span><span class="sxs-lookup"><span data-stu-id="5a5db-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a5db-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5a5db-132">Requirements</span></span>



| <span data-ttu-id="5a5db-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5a5db-133">Requirement</span></span> | <span data-ttu-id="5a5db-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5a5db-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5db-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a5db-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5a5db-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a5db-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a5db-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a5db-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5a5db-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a5db-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a5db-139">Header</span><span class="sxs-lookup"><span data-stu-id="5a5db-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a5db-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a5db-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a5db-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a5db-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a5db-142">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5a5db-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5a5db-143">**делетестринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5a5db-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="5a5db-144">**инсертстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5a5db-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="5a5db-145">**селектстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5a5db-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="5a5db-146">**сесоризонталекстент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5a5db-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="5a5db-147">**WM \_ компареитем**</span><span class="sxs-lookup"><span data-stu-id="5a5db-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

