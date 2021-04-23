---
title: Сообщение EM_GETTEXTMODE (RichEdit. h)
description: Возвращает текущий текстовый режим и уровень отменяемого элемента управления расширенного редактирования.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Элементы управления Windows для EM_GETTEXTMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492006"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="73bc8-104">\_Сообщение ЖЕТТЕКСТМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="73bc8-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="73bc8-105">Возвращает текущий текстовый режим и уровень отменяемого элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="73bc8-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="73bc8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73bc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73bc8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73bc8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73bc8-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="73bc8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="73bc8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73bc8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73bc8-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="73bc8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73bc8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73bc8-111">Return value</span></span>

<span data-ttu-id="73bc8-112">Возвращаемое значение — это одно или несколько значений из типа перечисления [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="73bc8-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="73bc8-113">Значения указывают текущий текстовый режим и уровень отмены элемента управления.</span><span class="sxs-lookup"><span data-stu-id="73bc8-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="73bc8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73bc8-114">Requirements</span></span>



| <span data-ttu-id="73bc8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="73bc8-115">Requirement</span></span> | <span data-ttu-id="73bc8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="73bc8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73bc8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73bc8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73bc8-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73bc8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73bc8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73bc8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73bc8-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73bc8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73bc8-121">Header</span><span class="sxs-lookup"><span data-stu-id="73bc8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73bc8-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="73bc8-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73bc8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73bc8-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="73bc8-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="73bc8-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73bc8-125">**EM \_ сеттекстмоде**</span><span class="sxs-lookup"><span data-stu-id="73bc8-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="73bc8-126">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="73bc8-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





