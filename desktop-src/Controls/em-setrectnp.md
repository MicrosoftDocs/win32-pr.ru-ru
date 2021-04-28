---
title: Сообщение EM_SETRECTNP (Winuser. h)
description: EM_SETRECTNP сообщение — задает прямоугольник форматирования для многострочного элемента управления Edit.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Элементы управления Windows для EM_SETRECTNP сообщений
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a8c85d4f7abd58ed3adb33ede66254c190a7bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085992"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="a633d-104">\_Сообщение СЕТРЕКТНП EM</span><span class="sxs-lookup"><span data-stu-id="a633d-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="a633d-105">Задает [прямоугольник форматирования](about-edit-controls.md) для многострочного элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a633d-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="a633d-106">Сообщение **EM \_ сетректнп** идентично сообщению [**\_ SETRECT EM**](em-setrect.md) , за исключением того, что **EM \_ сетректнп** *не перерисовывает* окно элемента управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="a633d-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="a633d-107">Прямоугольник форматирования — это ограничивающий прямоугольник, в который элемент управления рисует текст.</span><span class="sxs-lookup"><span data-stu-id="a633d-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="a633d-108">Ограничивающий прямоугольник не зависит от размера окна элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a633d-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="a633d-109">Это сообщение обрабатывается только многострочными элементами управления Edit.</span><span class="sxs-lookup"><span data-stu-id="a633d-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="a633d-110">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a633d-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a633d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a633d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a633d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a633d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a633d-113">**Расширенное редактирование 3,0 и более поздних версий:** Указывает, содержит ли новый прямоугольник абсолютные или относительные координаты.</span><span class="sxs-lookup"><span data-stu-id="a633d-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="a633d-114">Нулевое значение обозначает абсолютные координаты.</span><span class="sxs-lookup"><span data-stu-id="a633d-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="a633d-115">Значение 1 указывает смещения относительно текущего прямоугольника форматирования.</span><span class="sxs-lookup"><span data-stu-id="a633d-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="a633d-116">(Смещение может быть положительным или отрицательным.)</span><span class="sxs-lookup"><span data-stu-id="a633d-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="a633d-117">**Изменить элементы управления:** Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a633d-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a633d-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a633d-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a633d-119">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую новые размеры прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a633d-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="a633d-120">Если этот параметр имеет **значение NULL**, то для прямоугольника форматирования задаются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a633d-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a633d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a633d-121">Return value</span></span>

<span data-ttu-id="a633d-122">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a633d-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a633d-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="a633d-123">Remarks</span></span>

<span data-ttu-id="a633d-124">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 3,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a633d-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="a633d-125">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a633d-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a633d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a633d-126">Requirements</span></span>



| <span data-ttu-id="a633d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a633d-127">Requirement</span></span> | <span data-ttu-id="a633d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a633d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a633d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a633d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a633d-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a633d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a633d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a633d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a633d-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a633d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a633d-133">Header</span><span class="sxs-lookup"><span data-stu-id="a633d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a633d-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a633d-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a633d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a633d-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a633d-136">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="a633d-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a633d-137">**EM \_ SETRECT**</span><span class="sxs-lookup"><span data-stu-id="a633d-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="a633d-138">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="a633d-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a633d-139">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a633d-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

