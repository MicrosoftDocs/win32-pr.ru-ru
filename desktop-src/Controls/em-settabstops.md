---
title: Сообщение EM_SETTABSTOPS (Winuser. h)
description: Сообщение EM \_ сеттабстопс задает позицию табуляции в многострочном элементе управления Edit.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Элементы управления Windows для EM_SETTABSTOPS сообщений
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136254"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="dea47-104">\_Сообщение СЕТТАБСТОПС EM</span><span class="sxs-lookup"><span data-stu-id="dea47-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="dea47-105">Сообщение **EM \_ сеттабстопс** задает позицию табуляции в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="dea47-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="dea47-106">При копировании текста в элемент управления любой символ табуляции в тексте приводит к тому, что пространство будет создано до следующей позиции табуляции.</span><span class="sxs-lookup"><span data-stu-id="dea47-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="dea47-107">Это сообщение обрабатывается только многострочными элементами управления Edit.</span><span class="sxs-lookup"><span data-stu-id="dea47-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="dea47-108">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="dea47-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dea47-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dea47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea47-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dea47-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dea47-111">Количество единиц табуляции, содержащихся в массиве.</span><span class="sxs-lookup"><span data-stu-id="dea47-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="dea47-112">Если этот параметр равен нулю, параметр *lParam* игнорируется, а табуляция по умолчанию задается каждые 32 единиц шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="dea47-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="dea47-113">Если этот параметр равен 1, то позиции табуляции задаются для каждых *n* единиц шаблона диалогового окна, где *n* — расстояние, на которое указывает параметр *lParam* .</span><span class="sxs-lookup"><span data-stu-id="dea47-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="dea47-114">Если этот параметр больше 1, *lParam* является указателем на массив единиц табуляции.</span><span class="sxs-lookup"><span data-stu-id="dea47-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="dea47-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dea47-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dea47-116">Указатель на массив целых чисел без знака, указывающий позиции табуляции, в единицах шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="dea47-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="dea47-117">Если параметр *wParam* равен 1, этот параметр является указателем на целое число без знака, которое содержит расстояние между всеми позициями табуляции, в единицах шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="dea47-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea47-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dea47-118">Return value</span></span>

<span data-ttu-id="dea47-119">Если заданы все вкладки, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="dea47-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="dea47-120">Если все вкладки не заданы, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="dea47-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dea47-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dea47-121">Remarks</span></span>

<span data-ttu-id="dea47-122">Сообщение **EM \_ сеттабстопс** не перерисовывает окно элемента управления редактированием автоматически.</span><span class="sxs-lookup"><span data-stu-id="dea47-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="dea47-123">Если приложение изменяет позиции табуляции для текста, уже нарисованного в элементе управления "поле ввода", он должен вызвать функцию [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) для перерисовки окна управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="dea47-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="dea47-124">Значения, указанные в массиве, находятся в единицах шаблонов диалоговых окон, которые являются аппаратно-независимыми устройствами, используемыми в шаблонах диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="dea47-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="dea47-125">Чтобы преобразовать измерения из шаблона диалогового окна в единицы экрана (в пикселях), используйте функцию [**мапдиалогрект**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="dea47-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="dea47-126">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 3,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="dea47-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="dea47-127">Элемент управления Rich Edit может иметь максимальное количество заданных вкладок, заданное в параметре MAX \_ Tab Stop \_ .</span><span class="sxs-lookup"><span data-stu-id="dea47-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="dea47-128">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="dea47-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dea47-129">Требования</span><span class="sxs-lookup"><span data-stu-id="dea47-129">Requirements</span></span>



| <span data-ttu-id="dea47-130">Требование</span><span class="sxs-lookup"><span data-stu-id="dea47-130">Requirement</span></span> | <span data-ttu-id="dea47-131">Значение</span><span class="sxs-lookup"><span data-stu-id="dea47-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea47-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dea47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dea47-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dea47-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dea47-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dea47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dea47-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dea47-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dea47-136">Header</span><span class="sxs-lookup"><span data-stu-id="dea47-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea47-137"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dea47-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea47-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dea47-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="dea47-139">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="dea47-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dea47-140">**инвалидатерект**</span><span class="sxs-lookup"><span data-stu-id="dea47-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="dea47-141">**мапдиалогрект**</span><span class="sxs-lookup"><span data-stu-id="dea47-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

