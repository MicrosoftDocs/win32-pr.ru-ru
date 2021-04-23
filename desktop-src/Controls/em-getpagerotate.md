---
title: Сообщение EM_GETPAGEROTATE (RichEdit. h)
description: Возвращает макет текста для элемента управления Microsoft Rich Edit.
ms.assetid: 0efb112e-ad51-4ebb-9037-3aee3ab9ad1d
keywords:
- Элементы управления Windows для EM_GETPAGEROTATE сообщений
topic_type:
- apiref
api_name:
- EM_GETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7bc7cd3c77ae88cd4c8710e14b4472e57407ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492486"
---
# <a name="em_getpagerotate-message"></a><span data-ttu-id="b656f-104">\_Сообщение ЖЕТПАЖЕРОТАТЕ EM</span><span class="sxs-lookup"><span data-stu-id="b656f-104">EM\_GETPAGEROTATE message</span></span>

<span data-ttu-id="b656f-105">\[**EM \_ ЖЕТПАЖЕРОТАТЕ** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b656f-105">\[**EM\_GETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b656f-106">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="b656f-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b656f-107">Возвращает макет текста для элемента управления Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b656f-107">Gets the text layout for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b656f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b656f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b656f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b656f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b656f-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b656f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b656f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b656f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b656f-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b656f-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b656f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b656f-113">Return value</span></span>

<span data-ttu-id="b656f-114">Возвращает текущий макет текста.</span><span class="sxs-lookup"><span data-stu-id="b656f-114">Gets the current text layout.</span></span> <span data-ttu-id="b656f-115">Список возможных значений макета текста см. в разделе [**EM \_ сетпажеротате**](em-setpagerotate.md).</span><span class="sxs-lookup"><span data-stu-id="b656f-115">For a list of possible text layout values, see [**EM\_SETPAGEROTATE**](em-setpagerotate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b656f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b656f-116">Requirements</span></span>



| <span data-ttu-id="b656f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b656f-117">Requirement</span></span> | <span data-ttu-id="b656f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b656f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b656f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b656f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b656f-120">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="b656f-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b656f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b656f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b656f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b656f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b656f-123">Header</span><span class="sxs-lookup"><span data-stu-id="b656f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b656f-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b656f-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b656f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b656f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b656f-126">**EM \_ сетпажеротате**</span><span class="sxs-lookup"><span data-stu-id="b656f-126">**EM\_SETPAGEROTATE**</span></span>](em-setpagerotate.md)
</dt> </dl>

 

 





