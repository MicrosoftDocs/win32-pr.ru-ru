---
title: Сообщение CB_GETHORIZONTALEXTENT (Winuser. h)
description: Возвращает ширину (в пикселях), в которой окно списка можно прокручивать горизонтально (прокручиваемая ширина). Это применимо только в том случае, если в списке есть горизонтальная полоса прокрутки.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- Элементы управления Windows для CB_GETHORIZONTALEXTENT сообщений
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a2b1fb7c8fe7549360801516364528c9a2ef1f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071619"
---
# <a name="cb_gethorizontalextent-message"></a><span data-ttu-id="843d0-105">\_Сообщение ЖЕСОРИЗОНТАЛЕКСТЕНТ CB</span><span class="sxs-lookup"><span data-stu-id="843d0-105">CB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="843d0-106">Возвращает ширину (в пикселях), в которой окно списка можно прокручивать горизонтально (прокручиваемая ширина).</span><span class="sxs-lookup"><span data-stu-id="843d0-106">Gets the width, in pixels, that the list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="843d0-107">Это применимо только в том случае, если в списке есть горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="843d0-107">This is applicable only if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="843d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="843d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="843d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="843d0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="843d0-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="843d0-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="843d0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="843d0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="843d0-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="843d0-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="843d0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="843d0-113">Return value</span></span>

<span data-ttu-id="843d0-114">Возвращаемое значение является прокручиваемой шириной в пикселях.</span><span class="sxs-lookup"><span data-stu-id="843d0-114">The return value is the scrollable width, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="843d0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="843d0-115">Requirements</span></span>



| <span data-ttu-id="843d0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="843d0-116">Requirement</span></span> | <span data-ttu-id="843d0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="843d0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="843d0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="843d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="843d0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="843d0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="843d0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="843d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="843d0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="843d0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="843d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="843d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="843d0-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="843d0-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="843d0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="843d0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843d0-125">**\_СЕСОРИЗОНТАЛЕКСТЕНТ CB**</span><span class="sxs-lookup"><span data-stu-id="843d0-125">**CB\_SETHORIZONTALEXTENT**</span></span>](cb-sethorizontalextent.md)
</dt> </dl>

 

 





