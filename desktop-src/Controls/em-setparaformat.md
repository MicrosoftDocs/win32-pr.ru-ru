---
title: Сообщение EM_SETPARAFORMAT (RichEdit. h)
description: Задает форматирование абзаца для текущего выделения в элементе управления Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Элементы управления Windows для EM_SETPARAFORMAT сообщений
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490230"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="f2fde-104">\_Сообщение СЕТПАРАФОРМАТ EM</span><span class="sxs-lookup"><span data-stu-id="f2fde-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="f2fde-105">Задает форматирование абзаца для текущего выделения в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f2fde-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2fde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fde-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2fde-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2fde-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f2fde-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2fde-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2fde-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2fde-110">Указатель на структуру [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) с указанием новых атрибутов форматирования абзаца.</span><span class="sxs-lookup"><span data-stu-id="f2fde-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="f2fde-111">Изменяются только атрибуты, указанные членом **двмаск** .</span><span class="sxs-lookup"><span data-stu-id="f2fde-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="f2fde-112">Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , которая является РАСШИРЕНИЕМ структуры [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) данных.</span><span class="sxs-lookup"><span data-stu-id="f2fde-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="f2fde-113">Перед отправкой сообщения **EM \_ сетпараформат** установите элемент **кбсизе** в структуре, чтобы указать версию структуры.</span><span class="sxs-lookup"><span data-stu-id="f2fde-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fde-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2fde-114">Return value</span></span>

<span data-ttu-id="f2fde-115">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="f2fde-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f2fde-116">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f2fde-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fde-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f2fde-117">Requirements</span></span>



| <span data-ttu-id="f2fde-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f2fde-118">Requirement</span></span> | <span data-ttu-id="f2fde-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f2fde-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fde-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2fde-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2fde-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2fde-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2fde-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2fde-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2fde-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2fde-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2fde-124">Header</span><span class="sxs-lookup"><span data-stu-id="f2fde-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2fde-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2fde-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2fde-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2fde-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2fde-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f2fde-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2fde-128">\**ФОРМАТ \**</span><span class="sxs-lookup"><span data-stu-id="f2fde-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="f2fde-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="f2fde-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





