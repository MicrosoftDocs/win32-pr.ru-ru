---
title: Сообщение PGM_SETBUTTONSIZE (Коммктрл. h)
description: Задает текущий размер кнопки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетбуттонсизе пейджера.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Элементы управления Windows для PGM_SETBUTTONSIZE сообщений
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534031"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="b0440-105">\_Сообщение СЕТБУТТОНСИЗЕ PGM</span><span class="sxs-lookup"><span data-stu-id="b0440-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="b0440-106">Задает текущий размер кнопки для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="b0440-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="b0440-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетбуттонсизе пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="b0440-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0440-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0440-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0440-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0440-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b0440-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b0440-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b0440-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0440-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0440-112">Значение типа **int** , которое содержит новый размер кнопки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b0440-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0440-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0440-113">Return value</span></span>

<span data-ttu-id="b0440-114">Возвращает значение **типа int** , которое содержит размер предыдущей кнопки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b0440-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0440-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0440-115">Remarks</span></span>

<span data-ttu-id="b0440-116">Если элемент управления страничного навигатора имеет стиль [**ПГС \_ горизонтали**](pager-control-styles.md) , размер кнопки определяет ширину кнопок страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="b0440-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="b0440-117">Если элемент управления страничного навигатора имеет стиль [**ПГС по \_ вертикали**](pager-control-styles.md) , размер кнопки определяет высоту кнопок страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="b0440-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="b0440-118">По умолчанию элемент управления страничного навигатора устанавливает размер кнопки в три четверти ширины полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b0440-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="b0440-119">В текущий момент кнопка страничного навигатора имеет минимальный размер (12 пикселей).</span><span class="sxs-lookup"><span data-stu-id="b0440-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="b0440-120">Однако это может измениться, поэтому не следует зависеть от этого значения.</span><span class="sxs-lookup"><span data-stu-id="b0440-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0440-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b0440-121">Requirements</span></span>



| <span data-ttu-id="b0440-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b0440-122">Requirement</span></span> | <span data-ttu-id="b0440-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b0440-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0440-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0440-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0440-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0440-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0440-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0440-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0440-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0440-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0440-128">Header</span><span class="sxs-lookup"><span data-stu-id="b0440-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0440-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0440-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0440-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0440-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0440-131">**\_ЖЕТБУТТОНСИЗЕ PGM**</span><span class="sxs-lookup"><span data-stu-id="b0440-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





