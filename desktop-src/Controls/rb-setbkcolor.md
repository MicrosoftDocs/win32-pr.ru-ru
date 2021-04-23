---
title: Сообщение RB_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона элемента управления главной панели по умолчанию.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Элементы управления Windows для RB_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654541"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="386cc-104">\_Сообщение СЕТБККОЛОР RB</span><span class="sxs-lookup"><span data-stu-id="386cc-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="386cc-105">Задает цвет фона элемента управления главной панели по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="386cc-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="386cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="386cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="386cc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="386cc-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="386cc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="386cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="386cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="386cc-110">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее новый цвет фона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="386cc-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="386cc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="386cc-111">Return value</span></span>

<span data-ttu-id="386cc-112">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее предыдущий цвет фона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="386cc-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="386cc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="386cc-113">Remarks</span></span>

<span data-ttu-id="386cc-114">Цвет фона по умолчанию элемента управления главной панели используется для рисования фона в элементе управления главной панели и всех полос, добавленных после отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="386cc-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="386cc-115">Цвет фона по умолчанию для определенного диапазона можно переопределить при добавлении или изменении диапазона, установив \_ флаг рббим Colors в **фмаск** и установив **клрбакк** в структуре [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="386cc-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="386cc-116">Если стили оформления включены, это сообщение не действует.</span><span class="sxs-lookup"><span data-stu-id="386cc-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="386cc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="386cc-117">Requirements</span></span>



| <span data-ttu-id="386cc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="386cc-118">Requirement</span></span> | <span data-ttu-id="386cc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="386cc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="386cc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="386cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="386cc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="386cc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="386cc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="386cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="386cc-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="386cc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="386cc-124">Header</span><span class="sxs-lookup"><span data-stu-id="386cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="386cc-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="386cc-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="386cc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="386cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386cc-127">**\_ЖЕТБККОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="386cc-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

