---
title: Сообщение EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Вызывает функцию обратного вызова автозамены, которая хранится в \_ сообщении СЕТАУТОКОРРЕКТПРОК EM при условии, что текст, предшествующий точке вставки, является кандидатом на автозамену.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Элементы управления Windows для EM_CALLAUTOCORRECTPROC сообщений
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491517"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="57078-104">\_Сообщение КАЛЛАУТОКОРРЕКТПРОК EM</span><span class="sxs-lookup"><span data-stu-id="57078-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="57078-105">Вызывает функцию обратного вызова автозамены, которая хранится в сообщении [**\_ сетаутокорректпрок EM**](em-setautocorrectproc.md) при условии, что текст, предшествующий точке вставки, является кандидатом на автозамену.</span><span class="sxs-lookup"><span data-stu-id="57078-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="57078-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57078-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57078-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57078-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57078-108">Символ типа **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="57078-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="57078-109">Если этот символ является вкладкой (U + 0009), а символ, предшествующий точке вставки, — t a TAB, то символ, предшествующий точке вставки, обрабатывается как часть строки кандидатов для автозамены, а не как разделитель строк. в противном случае *wParam* не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="57078-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="57078-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57078-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57078-111">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="57078-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57078-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57078-112">Return value</span></span>

<span data-ttu-id="57078-113">Возвращаемое значение равно нулю, если сообщение прошло удачно, или ненулевой при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="57078-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="57078-114">Требования</span><span class="sxs-lookup"><span data-stu-id="57078-114">Requirements</span></span>



| <span data-ttu-id="57078-115">Требование</span><span class="sxs-lookup"><span data-stu-id="57078-115">Requirement</span></span> | <span data-ttu-id="57078-116">Значение</span><span class="sxs-lookup"><span data-stu-id="57078-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57078-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57078-117">Minimum supported client</span></span><br/> | <span data-ttu-id="57078-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57078-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="57078-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57078-119">Minimum supported server</span></span><br/> | <span data-ttu-id="57078-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57078-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57078-121">Header</span><span class="sxs-lookup"><span data-stu-id="57078-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="57078-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57078-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57078-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57078-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57078-124">*аутокорректпрок*</span><span class="sxs-lookup"><span data-stu-id="57078-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="57078-125">**EM \_ жетаутокорректпрок**</span><span class="sxs-lookup"><span data-stu-id="57078-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="57078-126">**EM \_ сетаутокорректпрок**</span><span class="sxs-lookup"><span data-stu-id="57078-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





