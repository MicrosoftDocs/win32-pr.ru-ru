---
title: Сообщение EM_GETPARAFORMAT (RichEdit. h)
description: Извлекает форматирование абзаца текущего выделения в элементе управления Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Элементы управления Windows для EM_GETPARAFORMAT сообщений
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989192"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="9149c-104">\_Сообщение ЖЕТПАРАФОРМАТ EM</span><span class="sxs-lookup"><span data-stu-id="9149c-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="9149c-105">Извлекает форматирование абзаца текущего выделения в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9149c-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9149c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9149c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9149c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9149c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9149c-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9149c-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9149c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9149c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9149c-110">Указатель на структуру [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) с параметром, которая получает атрибуты форматирования абзаца для текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="9149c-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="9149c-111">Если выбрано более одного абзаца, то структура получает атрибуты первого абзаца, а элемент **двмаск** указывает, какие атрибуты согласованы по всему выделению.</span><span class="sxs-lookup"><span data-stu-id="9149c-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="9149c-112">Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , которая является РАСШИРЕНИЕМ структуры [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) данных.</span><span class="sxs-lookup"><span data-stu-id="9149c-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="9149c-113">Перед отправкой сообщения **EM \_ жетпараформат** установите элемент **кбсизе** в структуре, чтобы указать версию структуры.</span><span class="sxs-lookup"><span data-stu-id="9149c-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9149c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9149c-114">Return value</span></span>

<span data-ttu-id="9149c-115">Это сообщение возвращает значение элемента **двмаск** структуры [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) данных.</span><span class="sxs-lookup"><span data-stu-id="9149c-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9149c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9149c-116">Requirements</span></span>



| <span data-ttu-id="9149c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9149c-117">Requirement</span></span> | <span data-ttu-id="9149c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9149c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9149c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9149c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9149c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9149c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9149c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9149c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9149c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9149c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9149c-123">Header</span><span class="sxs-lookup"><span data-stu-id="9149c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9149c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9149c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9149c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9149c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9149c-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9149c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9149c-127">\**ФОРМАТ \**</span><span class="sxs-lookup"><span data-stu-id="9149c-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="9149c-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="9149c-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





