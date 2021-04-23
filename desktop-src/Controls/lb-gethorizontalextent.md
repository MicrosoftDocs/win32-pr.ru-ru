---
title: Сообщение LB_GETHORIZONTALEXTENT (Winuser. h)
description: Возвращает ширину (в пикселях), с которой окно списка можно прокручивать горизонтально (прокручиваемую ширину), если в списке есть горизонтальная полоса прокрутки.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Элементы управления Windows для LB_GETHORIZONTALEXTENT сообщений
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989293"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="30e04-104">Сообщение жесоризонталекстент балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="30e04-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="30e04-105">Возвращает ширину (в пикселях), с которой окно списка можно прокручивать горизонтально (прокручиваемую ширину), если в списке есть горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="30e04-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="30e04-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30e04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30e04-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e04-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="30e04-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="30e04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30e04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e04-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="30e04-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e04-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30e04-111">Return value</span></span>

<span data-ttu-id="30e04-112">Возвращаемое значение — это прокручиваемая ширина (в пикселях) поля со списком.</span><span class="sxs-lookup"><span data-stu-id="30e04-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e04-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30e04-113">Remarks</span></span>

<span data-ttu-id="30e04-114">Чтобы ответить на сообщение **\_ жесоризонталекстент балансировки нагрузки** , список должен быть определен с помощью стиля [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="30e04-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="30e04-115">Если приложение не устанавливает горизонтальный экстент списка (с помощью [**балансировки нагрузки \_ сесоризонталекстент**](lb-sethorizontalextent.md)), горизонтальный экстент по умолчанию равен нулю.</span><span class="sxs-lookup"><span data-stu-id="30e04-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="30e04-116">Обратите внимание, что поле со списком динамически не обновляет область по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="30e04-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e04-117">Требования</span><span class="sxs-lookup"><span data-stu-id="30e04-117">Requirements</span></span>



| <span data-ttu-id="30e04-118">Требование</span><span class="sxs-lookup"><span data-stu-id="30e04-118">Requirement</span></span> | <span data-ttu-id="30e04-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30e04-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30e04-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30e04-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30e04-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30e04-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30e04-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30e04-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30e04-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30e04-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30e04-124">Header</span><span class="sxs-lookup"><span data-stu-id="30e04-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30e04-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30e04-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e04-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30e04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e04-127">**сесоризонталекстент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="30e04-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

