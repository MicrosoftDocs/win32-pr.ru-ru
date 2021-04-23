---
title: Сообщение EM_GETTEXTLENGTHEX (RichEdit. h)
description: Вычисляет длину текста различными способами. Обычно он вызывается перед созданием буфера для получения текста из элемента управления.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Элементы управления Windows для EM_GETTEXTLENGTHEX сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891833"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="8e0c8-105">\_Сообщение ЖЕТТЕКСТЛЕНГСЕКС EM</span><span class="sxs-lookup"><span data-stu-id="8e0c8-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="8e0c8-106">Вычисляет длину текста различными способами.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-106">Calculates text length in various ways.</span></span> <span data-ttu-id="8e0c8-107">Обычно он вызывается перед созданием буфера для получения текста из элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e0c8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e0c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e0c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e0c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e0c8-110">Указатель на структуру [**жеттекстленгсекс**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) , которая получает сведения о длине текста.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="8e0c8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e0c8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e0c8-112">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e0c8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e0c8-113">Return value</span></span>

<span data-ttu-id="8e0c8-114">Сообщение возвращает количество элементов **TCHAR** в элементе управления "поле ввода" в зависимости от настроек флагов в структуре [**жеттекстленгсекс**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) .</span><span class="sxs-lookup"><span data-stu-id="8e0c8-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="8e0c8-115">Если в элементе **flags** заданы несовместимые флаги, сообщение возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="8e0c8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e0c8-116">Remarks</span></span>

<span data-ttu-id="8e0c8-117">Это сообщение позволяет быстро и просто определить количество символов в версии элемента управления Rich Edit в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="8e0c8-118">Однако для целевой кодовой страницы, отличной от Юникода, возможно преобразование в сочетание однобайтовых и двухбайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e0c8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8e0c8-119">Requirements</span></span>



| <span data-ttu-id="8e0c8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8e0c8-120">Requirement</span></span> | <span data-ttu-id="8e0c8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8e0c8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0c8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e0c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e0c8-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e0c8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e0c8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e0c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e0c8-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e0c8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e0c8-126">Header</span><span class="sxs-lookup"><span data-stu-id="8e0c8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e0c8-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e0c8-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e0c8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e0c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e0c8-129">**жеттекстленгсекс**</span><span class="sxs-lookup"><span data-stu-id="8e0c8-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





