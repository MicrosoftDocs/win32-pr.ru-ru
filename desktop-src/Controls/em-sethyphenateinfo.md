---
title: Сообщение EM_SETHYPHENATEINFO (RichEdit. h)
description: Задает способ расстановки переносов в элементе управления Rich Edit.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Элементы управления Windows для EM_SETHYPHENATEINFO сообщений
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892481"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="e2980-104">\_Сообщение СЕСИФЕНАТЕИНФО EM</span><span class="sxs-lookup"><span data-stu-id="e2980-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="e2980-105">Задает способ расстановки переносов в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e2980-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2980-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2980-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2980-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2980-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2980-108">Указатель на структуру [**хифенатеинфо**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="e2980-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2980-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2980-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2980-110">Не используется, должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e2980-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2980-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2980-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2980-112">Чтобы включить расстановку переносов, клиент должен вызвать [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md), указав для \_ адванцедтипографи.</span><span class="sxs-lookup"><span data-stu-id="e2980-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2980-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e2980-113">Requirements</span></span>



| <span data-ttu-id="e2980-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e2980-114">Requirement</span></span> | <span data-ttu-id="e2980-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e2980-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2980-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2980-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2980-117">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2980-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2980-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2980-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2980-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2980-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2980-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2980-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2980-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2980-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2980-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2980-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2980-123">**EM \_ жесифенатеинфо**</span><span class="sxs-lookup"><span data-stu-id="e2980-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





