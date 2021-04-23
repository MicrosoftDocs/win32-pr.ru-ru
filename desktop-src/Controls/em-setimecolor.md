---
title: Сообщение EM_SETIMECOLOR (RichEdit. h)
description: Задает цвет композиции редактора методов ввода (IME) для элемента управления Rich Edit.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- Элементы управления Windows для EM_SETIMECOLOR сообщений
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491214"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="b13c9-104">\_Сообщение СЕТИМЕКОЛОР EM</span><span class="sxs-lookup"><span data-stu-id="b13c9-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="b13c9-105">Задает цвет композиции редактора методов ввода (IME) для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b13c9-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="b13c9-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="b13c9-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="b13c9-107">Он не поддерживается в каких-либо более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b13c9-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="b13c9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b13c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b13c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b13c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b13c9-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b13c9-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b13c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b13c9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b13c9-112">Указатель на структуру [**компколор**](/windows/desktop/api/Richedit/ns-richedit-compcolor) , содержащую заданный цвет композиции.</span><span class="sxs-lookup"><span data-stu-id="b13c9-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b13c9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b13c9-113">Return value</span></span>

<span data-ttu-id="b13c9-114">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="b13c9-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b13c9-115">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b13c9-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b13c9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b13c9-116">Requirements</span></span>



| <span data-ttu-id="b13c9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b13c9-117">Requirement</span></span> | <span data-ttu-id="b13c9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b13c9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b13c9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b13c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b13c9-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b13c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b13c9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b13c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b13c9-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b13c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b13c9-123">Header</span><span class="sxs-lookup"><span data-stu-id="b13c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b13c9-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b13c9-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b13c9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b13c9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b13c9-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b13c9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b13c9-127">**EM \_ жетимеколор**</span><span class="sxs-lookup"><span data-stu-id="b13c9-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="b13c9-128">**компколор**</span><span class="sxs-lookup"><span data-stu-id="b13c9-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





