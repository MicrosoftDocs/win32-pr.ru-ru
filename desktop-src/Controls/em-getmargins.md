---
title: Сообщение EM_GETMARGINS (Winuser. h)
description: Возвращает ширину левого и правого полей для элемента управления "поле ввода".
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Элементы управления Windows для EM_GETMARGINS сообщений
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801373"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="8fef5-104">\_Сообщение EM прибыли</span><span class="sxs-lookup"><span data-stu-id="8fef5-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="8fef5-105">Возвращает ширину левого и правого полей для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="8fef5-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fef5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fef5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fef5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fef5-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8fef5-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8fef5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fef5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fef5-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8fef5-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fef5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fef5-111">Return value</span></span>

<span data-ttu-id="8fef5-112">Возвращает ширину левого поля в ЛОВОРД и ширину правого поля в HIWORD.</span><span class="sxs-lookup"><span data-stu-id="8fef5-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fef5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fef5-113">Remarks</span></span>

<span data-ttu-id="8fef5-114">**Расширенное редактирование:** Сообщение **EM \_ прибыли** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8fef5-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fef5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8fef5-115">Requirements</span></span>



| <span data-ttu-id="8fef5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8fef5-116">Requirement</span></span> | <span data-ttu-id="8fef5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8fef5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fef5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fef5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8fef5-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fef5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fef5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fef5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8fef5-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fef5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fef5-122">Header</span><span class="sxs-lookup"><span data-stu-id="8fef5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fef5-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fef5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fef5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fef5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fef5-125">**EM \_ сетмаргинс**</span><span class="sxs-lookup"><span data-stu-id="8fef5-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





