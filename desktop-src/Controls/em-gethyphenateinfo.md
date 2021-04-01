---
title: Сообщение EM_GETHYPHENATEINFO (RichEdit. h)
description: Получает сведения о расстановке переносов для элемента управления форматированного ввода (Майкрософт).
ms.assetid: 70ccb698-e440-493b-8f38-2bf7f32e4b26
keywords:
- Элементы управления Windows для EM_GETHYPHENATEINFO сообщений
topic_type:
- apiref
api_name:
- EM_GETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d083b4bbc4b6854f767395d51dd9899c2a185d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071822"
---
# <a name="em_gethyphenateinfo-message"></a><span data-ttu-id="68746-104">\_Сообщение ЖЕСИФЕНАТЕИНФО EM</span><span class="sxs-lookup"><span data-stu-id="68746-104">EM\_GETHYPHENATEINFO message</span></span>

<span data-ttu-id="68746-105">Получает сведения о расстановке переносов для элемента управления форматированного ввода (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="68746-105">Retrieves information about hyphenation for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="68746-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68746-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68746-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68746-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68746-108">Структура [**хифенатеинфо**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="68746-108">The [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="68746-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68746-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68746-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="68746-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68746-111">Требования</span><span class="sxs-lookup"><span data-stu-id="68746-111">Requirements</span></span>



| <span data-ttu-id="68746-112">Требование</span><span class="sxs-lookup"><span data-stu-id="68746-112">Requirement</span></span> | <span data-ttu-id="68746-113">Значение</span><span class="sxs-lookup"><span data-stu-id="68746-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68746-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68746-114">Minimum supported client</span></span><br/> | <span data-ttu-id="68746-115">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="68746-115">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68746-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68746-116">Minimum supported server</span></span><br/> | <span data-ttu-id="68746-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68746-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68746-118">Header</span><span class="sxs-lookup"><span data-stu-id="68746-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="68746-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="68746-119"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68746-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68746-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68746-121">**EM \_ сесифенатеинфо**</span><span class="sxs-lookup"><span data-stu-id="68746-121">**EM\_SETHYPHENATEINFO**</span></span>](em-sethyphenateinfo.md)
</dt> </dl>

 

 





