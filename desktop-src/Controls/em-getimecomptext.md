---
title: Сообщение EM_GETIMECOMPTEXT (RichEdit. h)
description: Извлекает текст композиции редактора метода ввода (IME).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Элементы управления Windows для EM_GETIMECOMPTEXT сообщений
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989012"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="5a465-104">\_Сообщение ЖЕТИМЕКОМПТЕКСТ EM</span><span class="sxs-lookup"><span data-stu-id="5a465-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="5a465-105">Извлекает текст композиции редактора метода ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="5a465-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a465-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a465-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a465-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a465-108">Структура [**имекомптекст**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .</span><span class="sxs-lookup"><span data-stu-id="5a465-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a465-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a465-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a465-110">Буфер, который получает текст композиции.</span><span class="sxs-lookup"><span data-stu-id="5a465-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="5a465-111">Размер этого буфера содержится в элементе **CB** структуры *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5a465-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a465-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a465-112">Return value</span></span>

<span data-ttu-id="5a465-113">В случае успеха возвращаемое значение представляет собой число символов Юникода, скопированных в буфер.</span><span class="sxs-lookup"><span data-stu-id="5a465-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="5a465-114">В противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="5a465-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a465-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a465-115">Remarks</span></span>

<span data-ttu-id="5a465-116">Это сообщение принимает только строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5a465-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="5a465-117">**Предупреждение системы безопасности:** Убедитесь в наличии буфера, достаточного для размера входных данных.</span><span class="sxs-lookup"><span data-stu-id="5a465-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="5a465-118">В противном случае могут возникнуть проблемы с приложением.</span><span class="sxs-lookup"><span data-stu-id="5a465-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a465-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5a465-119">Requirements</span></span>



| <span data-ttu-id="5a465-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5a465-120">Requirement</span></span> | <span data-ttu-id="5a465-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5a465-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a465-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a465-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5a465-123">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a465-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a465-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a465-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5a465-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a465-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a465-126">Header</span><span class="sxs-lookup"><span data-stu-id="5a465-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a465-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a465-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a465-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a465-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a465-129">**имекомптекст**</span><span class="sxs-lookup"><span data-stu-id="5a465-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





