---
title: Сообщение RB_SETTEXTCOLOR (Коммктрл. h)
description: Задает цвет текста по умолчанию для элемента управления главной панели.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Элементы управления Windows для RB_SETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491751"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="e987f-104">\_Сообщение СЕТТЕКСТКОЛОР RB</span><span class="sxs-lookup"><span data-stu-id="e987f-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="e987f-105">Задает цвет текста по умолчанию для элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="e987f-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="e987f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e987f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e987f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e987f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e987f-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e987f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e987f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e987f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e987f-110">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее новый цвет текста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e987f-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e987f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e987f-111">Return value</span></span>

<span data-ttu-id="e987f-112">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее предыдущий цвет текста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e987f-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e987f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e987f-113">Remarks</span></span>

<span data-ttu-id="e987f-114">Цвет текста по умолчанию элемента управления главной панели используется для рисования текста в элементе управления "Главная панель" и всех полос, добавленных после отправки этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="e987f-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="e987f-115">Цвет текста по умолчанию для определенного диапазона можно переопределить при добавлении или изменении диапазона, установив \_ флаг рббим Colors в **фмаск** и установив **клрбакк** в структуре [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e987f-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e987f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e987f-116">Requirements</span></span>



| <span data-ttu-id="e987f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e987f-117">Requirement</span></span> | <span data-ttu-id="e987f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e987f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e987f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e987f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e987f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e987f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e987f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e987f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e987f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e987f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e987f-123">Header</span><span class="sxs-lookup"><span data-stu-id="e987f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e987f-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e987f-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e987f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e987f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e987f-126">**\_ЖЕТТЕКСТКОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="e987f-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

