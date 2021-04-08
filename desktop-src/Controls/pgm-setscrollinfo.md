---
title: Сообщение PGM_SETSCROLLINFO (Коммктрл. h)
description: Задает параметры прокрутки элемента управления страничного навигатора, включая значение времени ожидания, строки за время ожидания и количество пикселов в строке. Это сообщение можно отправить явным образом или с помощью \_ макроса пейджера сетскроллинфо.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Элементы управления Windows для PGM_SETSCROLLINFO сообщений
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891778"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="2d8d0-105">\_Сообщение СЕТСКРОЛЛИНФО PGM</span><span class="sxs-lookup"><span data-stu-id="2d8d0-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="2d8d0-106">\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="2d8d0-107">Это сообщение может не поддерживаться в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d8d0-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="2d8d0-108">Задает параметры прокрутки элемента управления страничного навигатора, включая значение времени ожидания, строки за время ожидания и количество пикселов в строке.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="2d8d0-109">Это сообщение можно отправить явным образом или с помощью макроса [**пейджера \_ сетскроллинфо**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="2d8d0-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d8d0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d8d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d8d0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d8d0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d8d0-112">Значение типа **uint** , указывающее время ожидания для прокрутки (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="2d8d0-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2d8d0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d8d0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d8d0-114">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **uint** , указывающий количество строк для прокрутки за время ожидания.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="2d8d0-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это **uint** , указывающий количество пикселей в строке.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d8d0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d8d0-116">Return value</span></span>

<span data-ttu-id="2d8d0-117">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="2d8d0-118">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="2d8d0-118">Security Considerations</span></span>

<span data-ttu-id="2d8d0-119">Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8d0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d8d0-120">Remarks</span></span>

<span data-ttu-id="2d8d0-121">Значение параметра время ожидания *wParam* определяет скорость, с которой элемент управления страничного навигатора создает события прокрутки, когда элемент управления захватывает ввод мыши, и нажата левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="2d8d0-122">Меньшие значения приводят к ускоренной прокрутке; большие значения приводят к низкой прокрутке.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="2d8d0-123">Значение по умолчанию — одна восьмая от времени двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="2d8d0-124">Дополнительные сведения см. в разделе [**жетдаублекликктиме**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span><span class="sxs-lookup"><span data-stu-id="2d8d0-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="2d8d0-125">По умолчанию при каждом событии прокрутки элемент управления страничный навигатор прокручивает сумму, равную всей ширине или высоте элемента управления, в зависимости от того, имеет ли элемент управления страничный навигатор горизонтальную или вертикальную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="2d8d0-126">Значения в параметре *lParam* используются для переопределения объема прокрутки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="2d8d0-127">Если указаны ненулевые значения, то величина прокрутки является произведением двух значений (ЛОВОРД (*lParam*) \* HIWORD (*lParam*)).</span><span class="sxs-lookup"><span data-stu-id="2d8d0-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d8d0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2d8d0-128">Requirements</span></span>



| <span data-ttu-id="2d8d0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2d8d0-129">Requirement</span></span> | <span data-ttu-id="2d8d0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2d8d0-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8d0-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d8d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8d0-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d8d0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d8d0-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d8d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8d0-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d8d0-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d8d0-135">Header</span><span class="sxs-lookup"><span data-stu-id="2d8d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d8d0-136"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d8d0-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d8d0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d8d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8d0-138">**Сетскроллинфо пейджера \_**</span><span class="sxs-lookup"><span data-stu-id="2d8d0-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

