---
title: Сообщение LB_INSERTSTRING (Winuser. h)
description: Вставляет строку или данные элемента в поле со списком. В отличие от сообщения ADDSTRING балансировки нагрузки \_ , \_ сообщение инсертстринг балансировки нагрузки не приводит к сортировке списка с сортировкой по фунтам \_ .
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- Элементы управления Windows для LB_INSERTSTRING сообщений
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137142"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="58353-105">Сообщение инсертстринг балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="58353-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="58353-106">Вставляет строку или данные элемента в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="58353-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="58353-107">В отличие от [**сообщения \_ ADDSTRING балансировки нагрузки**](lb-addstring.md) , сообщение **\_ инсертстринг балансировки нагрузки** не приводит к сортировке списка с [**\_ сортировкой по фунтам**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="58353-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="58353-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="58353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58353-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58353-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58353-110">Отсчитываемый от нуля индекс позиции, в которую вставляется строка.</span><span class="sxs-lookup"><span data-stu-id="58353-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="58353-111">Если этот параметр имеет значение-1, строка добавляется в конец списка.</span><span class="sxs-lookup"><span data-stu-id="58353-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="58353-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58353-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58353-113">Указатель на вставляемую строку, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="58353-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="58353-114">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , этот параметр сохраняется как данные элемента, а не как строка.</span><span class="sxs-lookup"><span data-stu-id="58353-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="58353-115">Вы можете отправить сообщения [**\_ жетитемдата**](lb-getitemdata.md) и [**\_ сетитемдата**](lb-setitemdata.md) балансировки нагрузки для получения или изменения данных элемента.</span><span class="sxs-lookup"><span data-stu-id="58353-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58353-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58353-116">Return value</span></span>

<span data-ttu-id="58353-117">Возвращаемое значение — это индекс позиции, в которую была вставлена строка.</span><span class="sxs-lookup"><span data-stu-id="58353-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="58353-118">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="58353-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="58353-119">Если недостаточно места для хранения новой строки, возвращается значение фунтов \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="58353-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="58353-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58353-120">Remarks</span></span>

<span data-ttu-id="58353-121">Сообщение [**\_ инитстораже балансировки нагрузки**](lb-initstorage.md) помогает ускорить инициализацию списков с большим количеством элементов (более 100).</span><span class="sxs-lookup"><span data-stu-id="58353-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="58353-122">Он резервирует указанный объем памяти, чтобы последующие сообщения **\_ Инсертстринги балансировки нагрузки** занимали кратчайшее время.</span><span class="sxs-lookup"><span data-stu-id="58353-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="58353-123">Для параметров *wParam* и *lParam* можно использовать оценки.</span><span class="sxs-lookup"><span data-stu-id="58353-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="58353-124">При чрезмерной оценке выделяется дополнительный объем памяти. Если недооценивать, то для элементов, превышающих запрошенный объем, используется нормальное выделение.</span><span class="sxs-lookup"><span data-stu-id="58353-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="58353-125">Если список имеет стиль [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) и вы вставили строку шире, чем поле списка, отправьте сообщение [**\_ сесоризонталекстент балансировки нагрузки**](lb-sethorizontalextent.md) , чтобы убедиться, что отображается горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="58353-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="58353-126">Для приложения ANSI система преобразует текст в поле со списком в Юникод с помощью команды CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="58353-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="58353-127">Это может вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="58353-127">This can cause problems.</span></span> <span data-ttu-id="58353-128">Например, римские символы с диакритическими знаками в списке не в Юникоде в японских окнах будут выступать из искажений.</span><span class="sxs-lookup"><span data-stu-id="58353-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="58353-129">Чтобы устранить эту проблему, либо скомпилируйте приложение как Юникод, либо используйте список, рисуемый владельцем.</span><span class="sxs-lookup"><span data-stu-id="58353-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="58353-130">Требования</span><span class="sxs-lookup"><span data-stu-id="58353-130">Requirements</span></span>



| <span data-ttu-id="58353-131">Требование</span><span class="sxs-lookup"><span data-stu-id="58353-131">Requirement</span></span> | <span data-ttu-id="58353-132">Значение</span><span class="sxs-lookup"><span data-stu-id="58353-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58353-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58353-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58353-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58353-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58353-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58353-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58353-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58353-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58353-137">Header</span><span class="sxs-lookup"><span data-stu-id="58353-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="58353-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58353-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58353-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58353-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="58353-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="58353-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="58353-141">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="58353-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="58353-142">**селектстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="58353-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="58353-143">**сесоризонталекстент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="58353-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

