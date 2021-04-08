---
title: Сообщение EM_GETRECT (Winuser. h)
description: Возвращает прямоугольник форматирования элемента управления "поле ввода".
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Элементы управления Windows для EM_GETRECT сообщений
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892058"
---
# <a name="em_getrect-message"></a><span data-ttu-id="52001-104">\_Сообщение EM</span><span class="sxs-lookup"><span data-stu-id="52001-104">EM\_GETRECT message</span></span>

<span data-ttu-id="52001-105">Возвращает [прямоугольник форматирования](about-edit-controls.md) элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="52001-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="52001-106">Прямоугольник форматирования — это ограничивающий прямоугольник, в который элемент управления рисует текст.</span><span class="sxs-lookup"><span data-stu-id="52001-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="52001-107">Ограничивающий прямоугольник не зависит от размера окна Edit-Control.</span><span class="sxs-lookup"><span data-stu-id="52001-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="52001-108">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="52001-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="52001-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="52001-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52001-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52001-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52001-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="52001-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52001-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52001-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52001-113">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает прямоугольник форматирования.</span><span class="sxs-lookup"><span data-stu-id="52001-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52001-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52001-114">Return value</span></span>

<span data-ttu-id="52001-115">Возвращаемое значение не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="52001-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="52001-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52001-116">Remarks</span></span>

<span data-ttu-id="52001-117">Можно изменить прямоугольник форматирования в многострочном элементе управления Edit с помощью сообщений [**EM \_ SETRECT**](em-setrect.md) и [**EM \_ сетректнп**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="52001-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="52001-118">При определенных условиях **EM может \_** не возвращать точные значения, которые [**\_ SETRECT EM**](em-setrect.md) или [**EM \_ сетректнп**](em-setrectnp.md) будут примерно верными, но могут быть отключены на несколько пикселей.</span><span class="sxs-lookup"><span data-stu-id="52001-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="52001-119">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="52001-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="52001-120">Прямоугольник форматирования не включает панель выбора, которая является непомеченной областью слева от каждого абзаца.</span><span class="sxs-lookup"><span data-stu-id="52001-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="52001-121">При щелчке на панели выбора линия выделяется.</span><span class="sxs-lookup"><span data-stu-id="52001-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="52001-122">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="52001-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52001-123">Требования</span><span class="sxs-lookup"><span data-stu-id="52001-123">Requirements</span></span>



| <span data-ttu-id="52001-124">Требование</span><span class="sxs-lookup"><span data-stu-id="52001-124">Requirement</span></span> | <span data-ttu-id="52001-125">Значение</span><span class="sxs-lookup"><span data-stu-id="52001-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52001-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52001-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52001-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52001-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52001-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52001-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52001-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52001-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52001-130">Header</span><span class="sxs-lookup"><span data-stu-id="52001-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="52001-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52001-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52001-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52001-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="52001-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="52001-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52001-134">**EM \_ SETRECT**</span><span class="sxs-lookup"><span data-stu-id="52001-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="52001-135">**EM \_ сетректнп**</span><span class="sxs-lookup"><span data-stu-id="52001-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="52001-136">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="52001-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="52001-137">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52001-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

