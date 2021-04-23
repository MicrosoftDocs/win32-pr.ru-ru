---
title: Сообщение EM_GETCHARFORMAT (RichEdit. h)
description: Определяет форматирование символов в элементе управления Rich Edit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Элементы управления Windows для EM_GETCHARFORMAT сообщений
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071708"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="10ec1-104">\_Сообщение ЖЕТЧАРФОРМАТ EM</span><span class="sxs-lookup"><span data-stu-id="10ec1-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="10ec1-105">Определяет форматирование символов в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="10ec1-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="10ec1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="10ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10ec1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10ec1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10ec1-108">Задает диапазон текста, из которого извлекается форматирование.</span><span class="sxs-lookup"><span data-stu-id="10ec1-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="10ec1-109">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="10ec1-109">It can be one of the following values.</span></span>



| <span data-ttu-id="10ec1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="10ec1-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="10ec1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="10ec1-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="10ec1-112"><dt>**\_по умолчанию — SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="10ec1-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="10ec1-113">Форматирование символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10ec1-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="10ec1-114"><dt>**Выбор параметров SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10ec1-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="10ec1-115">Форматирование символов текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="10ec1-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="10ec1-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10ec1-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10ec1-117">Структура [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) , которая получает атрибуты первого символа.</span><span class="sxs-lookup"><span data-stu-id="10ec1-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="10ec1-118">Элемент **двмаск** указывает, какие атрибуты согласованы по всему выделению.</span><span class="sxs-lookup"><span data-stu-id="10ec1-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="10ec1-119">Например, если все выделенные фрагменты выделены курсивом или не курсивом, то \_ устанавливается курсивом. Если выделение частично выделено курсивом, а частично нет, \_ значит, не задано значение CFM Italic.</span><span class="sxs-lookup"><span data-stu-id="10ec1-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="10ec1-120">Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , которая является расширением структуры [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="10ec1-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="10ec1-121">Перед отправкой сообщения **EM \_ жетчарформат** установите элемент **кбсизе** в структуре, чтобы указать версию структуры.</span><span class="sxs-lookup"><span data-stu-id="10ec1-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10ec1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10ec1-122">Return value</span></span>

<span data-ttu-id="10ec1-123">Это сообщение возвращает значение элемента **двмаск** структуры [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="10ec1-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ec1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="10ec1-124">Requirements</span></span>



| <span data-ttu-id="10ec1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="10ec1-125">Requirement</span></span> | <span data-ttu-id="10ec1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="10ec1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10ec1-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10ec1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10ec1-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10ec1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10ec1-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10ec1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10ec1-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10ec1-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10ec1-131">Header</span><span class="sxs-lookup"><span data-stu-id="10ec1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="10ec1-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="10ec1-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ec1-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10ec1-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="10ec1-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="10ec1-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10ec1-135">**чарформат**</span><span class="sxs-lookup"><span data-stu-id="10ec1-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="10ec1-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="10ec1-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





