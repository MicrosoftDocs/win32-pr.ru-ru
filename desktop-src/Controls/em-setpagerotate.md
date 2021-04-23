---
title: Сообщение EM_SETPAGEROTATE (RichEdit. h)
description: Задает макет текста для элемента управления Rich Edit.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Элементы управления Windows для EM_SETPAGEROTATE сообщений
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988554"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="4c7f7-104">\_Сообщение СЕТПАЖЕРОТАТЕ EM</span><span class="sxs-lookup"><span data-stu-id="4c7f7-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="4c7f7-105">\[**EM \_ СЕТПАЖЕРОТАТЕ** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c7f7-106">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="4c7f7-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="4c7f7-107">Задает макет текста для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c7f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c7f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c7f7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7f7-110">Значение макета текста.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-110">Text layout value.</span></span> <span data-ttu-id="4c7f7-111">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-111">This can be one of the following values.</span></span>



| <span data-ttu-id="4c7f7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4c7f7-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="4c7f7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4c7f7-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="4c7f7-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f7-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="4c7f7-115">Текст перетекает слева направо и сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="4c7f7-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f7-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="4c7f7-117">Текст перетекает снизу вверх и слева направо.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="4c7f7-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f7-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="4c7f7-119">Текст перетекает справа налево и снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="4c7f7-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f7-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="4c7f7-121">Текст перетекает сверху вниз и справа налево.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="4c7f7-122"><dt>**EPR \_ SE**</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f7-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="4c7f7-123">**Windows 8:** Направление текста сверху вниз и слева направо (разметка текста в формате монгольский).</span><span class="sxs-lookup"><span data-stu-id="4c7f7-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4c7f7-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c7f7-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7f7-125">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7f7-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c7f7-126">Return value</span></span>

<span data-ttu-id="4c7f7-127">Возвращаемое значение — новое значение макета текста.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7f7-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c7f7-128">Remarks</span></span>

<span data-ttu-id="4c7f7-129">Это сообщение задает макет текста для всего документа.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="4c7f7-130">Однако внедренное содержимое не поворачивается и должно быть повернуто отдельно приложением.</span><span class="sxs-lookup"><span data-stu-id="4c7f7-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7f7-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4c7f7-131">Requirements</span></span>



| <span data-ttu-id="4c7f7-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4c7f7-132">Requirement</span></span> | <span data-ttu-id="4c7f7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4c7f7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7f7-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c7f7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7f7-135">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c7f7-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c7f7-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c7f7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7f7-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c7f7-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c7f7-138">Header</span><span class="sxs-lookup"><span data-stu-id="4c7f7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c7f7-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f7-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7f7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c7f7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7f7-141">**EM \_ жетпажеротате**</span><span class="sxs-lookup"><span data-stu-id="4c7f7-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





