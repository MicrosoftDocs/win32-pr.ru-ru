---
title: Сообщение BM_SETSTYLE (Winuser. h)
description: Задает стиль кнопки. Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Элементы управления Windows для BM_SETSTYLE сообщений
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988378"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="3e8e3-105">\_Сообщение BM SETSTYLE</span><span class="sxs-lookup"><span data-stu-id="3e8e3-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="3e8e3-106">Задает стиль кнопки.</span><span class="sxs-lookup"><span data-stu-id="3e8e3-106">Sets the style of a button.</span></span> <span data-ttu-id="3e8e3-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .</span><span class="sxs-lookup"><span data-stu-id="3e8e3-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e8e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e8e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e8e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e8e3-110">Стиль кнопки.</span><span class="sxs-lookup"><span data-stu-id="3e8e3-110">The button style.</span></span> <span data-ttu-id="3e8e3-111">Этот параметр может быть сочетанием стилей кнопок.</span><span class="sxs-lookup"><span data-stu-id="3e8e3-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="3e8e3-112">Таблицу стилей кнопок см. в разделе [стили кнопок](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="3e8e3-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e8e3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e8e3-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e8e3-114">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) объекта *lParam* — это **логическое** значение, указывающее, следует ли перерисовать кнопку.</span><span class="sxs-lookup"><span data-stu-id="3e8e3-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="3e8e3-115">Значение **true** Перерисовывает кнопку; значение **false** не перерисовывает кнопку.</span><span class="sxs-lookup"><span data-stu-id="3e8e3-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8e3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e8e3-116">Return value</span></span>

<span data-ttu-id="3e8e3-117">Это сообщение всегда возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3e8e3-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8e3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3e8e3-118">Requirements</span></span>



| <span data-ttu-id="3e8e3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3e8e3-119">Requirement</span></span> | <span data-ttu-id="3e8e3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3e8e3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8e3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e8e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8e3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e8e3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3e8e3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e8e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8e3-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e8e3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e8e3-125">Header</span><span class="sxs-lookup"><span data-stu-id="3e8e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e8e3-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e8e3-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

