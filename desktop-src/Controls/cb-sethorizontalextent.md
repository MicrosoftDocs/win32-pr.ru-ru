---
title: Сообщение CB_SETHORIZONTALEXTENT (Winuser. h)
description: Приложение отправляет \_ сообщение СЕСОРИЗОНТАЛЕКСТЕНТ CB, чтобы задать ширину (в пикселях), на которую окно списка можно прокручивать горизонтально (прокручиваемую ширину).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Элементы управления Windows для CB_SETHORIZONTALEXTENT сообщений
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490521"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="49c03-104">\_Сообщение СЕСОРИЗОНТАЛЕКСТЕНТ CB</span><span class="sxs-lookup"><span data-stu-id="49c03-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="49c03-105">Приложение отправляет сообщение **\_ сесоризонталекстент CB** , чтобы задать ширину (в пикселях), на которую окно списка можно прокручивать горизонтально (прокручиваемую ширину).</span><span class="sxs-lookup"><span data-stu-id="49c03-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="49c03-106">Если ширина списка меньше этого значения, горизонтальная полоса прокрутки горизонтально прокручивает элементы списка.</span><span class="sxs-lookup"><span data-stu-id="49c03-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="49c03-107">Если ширина окна списка равна или больше этого значения, горизонтальная полоса прокрутки скрыта или, если поле со списком имеет стиль [**\_ дисабленоскролл CBS**](combo-box-styles.md) , отключено.</span><span class="sxs-lookup"><span data-stu-id="49c03-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="49c03-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49c03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49c03-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49c03-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49c03-110">Задает ширину прокручиваемого окна списка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="49c03-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49c03-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49c03-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="49c03-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49c03-113">Требования</span><span class="sxs-lookup"><span data-stu-id="49c03-113">Requirements</span></span>



| <span data-ttu-id="49c03-114">Требование</span><span class="sxs-lookup"><span data-stu-id="49c03-114">Requirement</span></span> | <span data-ttu-id="49c03-115">Значение</span><span class="sxs-lookup"><span data-stu-id="49c03-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c03-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49c03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49c03-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49c03-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49c03-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49c03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49c03-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49c03-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49c03-120">Header</span><span class="sxs-lookup"><span data-stu-id="49c03-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49c03-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49c03-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c03-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49c03-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c03-123">**\_ЖЕСОРИЗОНТАЛЕКСТЕНТ CB**</span><span class="sxs-lookup"><span data-stu-id="49c03-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 





