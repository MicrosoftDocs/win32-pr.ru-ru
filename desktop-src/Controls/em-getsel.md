---
title: Сообщение EM_GETSEL (Winuser. h)
description: Возвращает начальные и конечные позиции символов (в Тчарс) текущего выделения в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Элементы управления Windows для EM_GETSEL сообщений
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071564"
---
# <a name="em_getsel-message"></a><span data-ttu-id="85c61-105">\_Сообщение ЖЕТСЕЛ EM</span><span class="sxs-lookup"><span data-stu-id="85c61-105">EM\_GETSEL message</span></span>

<span data-ttu-id="85c61-106">Возвращает начальные и конечные позиции символов (в **файле TCHAR**) текущего выделения в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="85c61-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="85c61-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="85c61-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="85c61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85c61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85c61-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85c61-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85c61-110">Указатель на значение **DWORD** , получающее начальную точку выделения.</span><span class="sxs-lookup"><span data-stu-id="85c61-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="85c61-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="85c61-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85c61-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85c61-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85c61-113">Указатель на значение **DWORD** , которое получает позиции первого невыделенного символа после конца выделенного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="85c61-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="85c61-114">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="85c61-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85c61-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85c61-115">Return value</span></span>

<span data-ttu-id="85c61-116">Возвращаемое значение — это отсчитываемое от нуля значение с начальной позицией выбора в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и позицией первого файла **TCHAR** после последнего выбранного файла **TCHAR** в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85c61-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="85c61-117">Если одно из этих значений превышает 65 535, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="85c61-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="85c61-118">Лучше использовать значения, возвращаемые в *wParam* и *lParam* , так как они являются полными 32-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="85c61-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="85c61-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85c61-119">Remarks</span></span>

<span data-ttu-id="85c61-120">Если ничего не выделено, начальное и конечное значения являются обеим положением курсора.</span><span class="sxs-lookup"><span data-stu-id="85c61-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="85c61-121">**Элементы управления Rich Edit:** Для получения той же информации можно также использовать сообщение [**EM \_ ексжетсел**](em-exgetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="85c61-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="85c61-122">**EM \_ ЕКСЖЕТСЕЛ** также возвращает начальные и конечные позиции символов как 32-разрядные значения.</span><span class="sxs-lookup"><span data-stu-id="85c61-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="85c61-123">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="85c61-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="85c61-124">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="85c61-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85c61-125">Требования</span><span class="sxs-lookup"><span data-stu-id="85c61-125">Requirements</span></span>



| <span data-ttu-id="85c61-126">Требование</span><span class="sxs-lookup"><span data-stu-id="85c61-126">Requirement</span></span> | <span data-ttu-id="85c61-127">Значение</span><span class="sxs-lookup"><span data-stu-id="85c61-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c61-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85c61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="85c61-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85c61-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="85c61-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85c61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="85c61-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85c61-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85c61-132">Header</span><span class="sxs-lookup"><span data-stu-id="85c61-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c61-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85c61-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c61-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85c61-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="85c61-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="85c61-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="85c61-136">**EM \_ ексжетсел**</span><span class="sxs-lookup"><span data-stu-id="85c61-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="85c61-137">**EM \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="85c61-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 

