---
title: Сообщение EM_GETZOOM (RichEdit. h)
description: Возвращает текущее соотношение масштаба. Ъявлению масштаба всегда находится в диапазоне от 1/64 до 64. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Элементы управления Windows для EM_GETZOOM сообщений
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801372"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="96541-106">\_Сообщение о СОХРАНЕНИИ EM</span><span class="sxs-lookup"><span data-stu-id="96541-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="96541-107">Возвращает текущий коэффициент масштабирования для многострочного элемента управления "поле ввода" или элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="96541-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="96541-108">Ъявлению масштаба всегда находится в диапазоне от 1/64 до 64.</span><span class="sxs-lookup"><span data-stu-id="96541-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="96541-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="96541-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96541-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96541-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96541-111">Получает числитель коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="96541-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="96541-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96541-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96541-113">Получает знаменатель коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="96541-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96541-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96541-114">Return value</span></span>

<span data-ttu-id="96541-115">Сообщение возвращает **значение true** , если обрабатывается сообщение, которое будет иметь значение, если параметр *wParam* и *lParam* не равны **null**.</span><span class="sxs-lookup"><span data-stu-id="96541-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96541-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96541-116">Remarks</span></span>

<span data-ttu-id="96541-117">**Изменить:** Поддерживается в Windows 10 1809 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="96541-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="96541-118">В элементе управления "поле ввода" должен быть установлен расширенный набор стилей **ES \_ ex \_ масштабируемый** , чтобы это сообщение имело значение. см. раздел [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="96541-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="96541-119">Дополнительные сведения об элементе управления "поле ввода" см. в разделе [Edit Controls](edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="96541-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96541-120">Требования</span><span class="sxs-lookup"><span data-stu-id="96541-120">Requirements</span></span>



| <span data-ttu-id="96541-121">Требование</span><span class="sxs-lookup"><span data-stu-id="96541-121">Requirement</span></span> | <span data-ttu-id="96541-122">Значение</span><span class="sxs-lookup"><span data-stu-id="96541-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96541-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96541-123">Minimum supported client</span></span><br/> | <span data-ttu-id="96541-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96541-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96541-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96541-125">Minimum supported server</span></span><br/> | <span data-ttu-id="96541-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96541-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96541-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="96541-127">Redistributable</span></span><br/>          | <span data-ttu-id="96541-128">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="96541-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="96541-129">Header</span><span class="sxs-lookup"><span data-stu-id="96541-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="96541-130"><dt>RichEdit. h/Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="96541-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96541-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96541-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96541-132">**EM \_ сетзум**</span><span class="sxs-lookup"><span data-stu-id="96541-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 





