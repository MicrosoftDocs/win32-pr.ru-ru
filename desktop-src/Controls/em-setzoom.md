---
title: Сообщение EM_SETZOOM (RichEdit. h)
description: Задает коэффициент масштабирования. Соотношение должно быть числом в диапазоне от 1/64 до 64. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Элементы управления Windows для EM_SETZOOM сообщений
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892154"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="eefb4-106">\_Сообщение СЕТЗУМ EM</span><span class="sxs-lookup"><span data-stu-id="eefb4-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="eefb4-107">Задает коэффициент масштабирования для многострочного элемента управления "поле ввода" или элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="eefb4-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="eefb4-108">Соотношение должно быть числом в диапазоне от 1/64 до 64.</span><span class="sxs-lookup"><span data-stu-id="eefb4-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="eefb4-109">В элементе управления "поле ввода" должен быть установлен расширенный набор стилей **ES \_ ex \_ масштабируемый** , чтобы это сообщение имело значение. см. раздел [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="eefb4-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="eefb4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eefb4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eefb4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eefb4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eefb4-112">Числитель коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="eefb4-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="eefb4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eefb4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eefb4-114">Знаменатель коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="eefb4-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="eefb4-115">Эти параметры могут иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="eefb4-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="eefb4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="eefb4-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="eefb4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eefb4-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="eefb4-118"><dt>**Оба значения 0**</dt></span><span class="sxs-lookup"><span data-stu-id="eefb4-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="eefb4-119">Отключает масштаб с помощью сообщения **EM \_ сетзум** (по-прежнему может произойти с помощью [**тксжетекстент**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span><span class="sxs-lookup"><span data-stu-id="eefb4-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="eefb4-120"><dt>**1/64 < (wParam/lParam) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="eefb4-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="eefb4-121">Отображение масштаба с помощью числителя или знаменателя коэффициента масштабирования</span><span class="sxs-lookup"><span data-stu-id="eefb4-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eefb4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eefb4-122">Return value</span></span>

<span data-ttu-id="eefb4-123">Если новый параметр масштабирования принимается, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="eefb4-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="eefb4-124">Если новое значение масштаба не принято, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="eefb4-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefb4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eefb4-125">Remarks</span></span>

<span data-ttu-id="eefb4-126">**Изменить:** Поддерживается в Windows 10 1809 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="eefb4-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="eefb4-127">В элементе управления "поле ввода" должен быть установлен расширенный набор стилей **ES \_ ex \_ масштабируемый** , чтобы это сообщение имело значение. см. раздел [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="eefb4-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="eefb4-128">Дополнительные сведения об элементе управления "поле ввода" см. в разделе [Edit Controls](about-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="eefb4-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eefb4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="eefb4-129">Requirements</span></span>



| <span data-ttu-id="eefb4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="eefb4-130">Requirement</span></span> | <span data-ttu-id="eefb4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eefb4-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eefb4-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eefb4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eefb4-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eefb4-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eefb4-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eefb4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eefb4-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eefb4-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eefb4-136">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="eefb4-136">Redistributable</span></span><br/>          | <span data-ttu-id="eefb4-137">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="eefb4-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="eefb4-138">Header</span><span class="sxs-lookup"><span data-stu-id="eefb4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eefb4-139"><dt>RichEdit. h/Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eefb4-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefb4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eefb4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefb4-141">**EM для максимального \_ масштаба**</span><span class="sxs-lookup"><span data-stu-id="eefb4-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





