---
title: Сообщение EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Задает текущее состояние типографских параметров для элемента управления Rich Edit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Элементы управления Windows для EM_SETTYPOGRAPHYOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988820"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="7e6ce-104">\_Сообщение СЕТТИПОГРАФЙОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="7e6ce-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="7e6ce-105">Задает текущее состояние типографских параметров для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e6ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e6ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e6ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e6ce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e6ce-108">Задает одно или оба из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="7e6ce-109">Значение</span><span class="sxs-lookup"><span data-stu-id="7e6ce-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="7e6ce-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7e6ce-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="7e6ce-111"><dt>**Для \_ АДВАНЦЕДТИПОГРАФИ**</dt></span><span class="sxs-lookup"><span data-stu-id="7e6ce-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="7e6ce-112">Включено дополнительное разбиение строк и форматирование строк.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="7e6ce-113"><dt>**\_симплелинебреак**</dt></span><span class="sxs-lookup"><span data-stu-id="7e6ce-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="7e6ce-114">Более быстрое разбиение строк для простого текста (требуется **\_ адванцедтипографи**).</span><span class="sxs-lookup"><span data-stu-id="7e6ce-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="7e6ce-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e6ce-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e6ce-116">Маска, состоящая из одного или нескольких флагов в параметре *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="7e6ce-117">Будут установлены или сняты только флаги, установленные в этой маске.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="7e6ce-118">Это позволяет устанавливать или снимать один флаг без считывания текущих состояний флагов.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e6ce-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e6ce-119">Return value</span></span>

<span data-ttu-id="7e6ce-120">Возвращает **значение true** , если *wParam* является допустимым; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e6ce-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e6ce-121">Remarks</span></span>

<span data-ttu-id="7e6ce-122">При необходимости расширенное разбиение строк включается автоматически элементом управления Rich Editing, например для обработки сложных наборов символов, таких как арабский и иврит, а также для математики.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="7e6ce-123">Он также необходим для выравнивания абзацев, расстановки переносов и других типографских функций.</span><span class="sxs-lookup"><span data-stu-id="7e6ce-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6ce-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7e6ce-124">Requirements</span></span>



| <span data-ttu-id="7e6ce-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7e6ce-125">Requirement</span></span> | <span data-ttu-id="7e6ce-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7e6ce-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6ce-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e6ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7e6ce-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e6ce-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e6ce-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e6ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7e6ce-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e6ce-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e6ce-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7e6ce-131">Redistributable</span></span><br/>          | <span data-ttu-id="7e6ce-132">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="7e6ce-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="7e6ce-133">Header</span><span class="sxs-lookup"><span data-stu-id="7e6ce-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e6ce-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e6ce-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e6ce-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e6ce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e6ce-136">**EM \_ жеттипографйоптионс**</span><span class="sxs-lookup"><span data-stu-id="7e6ce-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 





