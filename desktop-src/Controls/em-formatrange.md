---
title: Сообщение EM_FORMATRANGE (RichEdit. h)
description: Форматирует диапазон текста в элементе управления расширенного редактирования для конкретного устройства.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Элементы управления Windows для EM_FORMATRANGE сообщений
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892065"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="ba47c-104">\_Сообщение ФОРМАТРАНЖЕ EM</span><span class="sxs-lookup"><span data-stu-id="ba47c-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="ba47c-105">Форматирует диапазон текста в элементе управления расширенного редактирования для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="ba47c-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba47c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba47c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba47c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba47c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba47c-108">Указывает, следует ли визуализировать текст.</span><span class="sxs-lookup"><span data-stu-id="ba47c-108">Specifies whether to render the text.</span></span> <span data-ttu-id="ba47c-109">Если этот параметр не равен нулю, текст подготавливается к просмотру.</span><span class="sxs-lookup"><span data-stu-id="ba47c-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="ba47c-110">В противном случае текст просто измеряется.</span><span class="sxs-lookup"><span data-stu-id="ba47c-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="ba47c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba47c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba47c-112">Структура [**форматранже**](/windows/desktop/api/Richedit/ns-richedit-formatrange) , содержащая сведения об устройстве вывода, или **значение NULL** для высвобождения информации, кэшированной элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ba47c-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba47c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba47c-113">Return value</span></span>

<span data-ttu-id="ba47c-114">Это сообщение возвращает индекс последнего символа, помещающийся в области, плюс 1.</span><span class="sxs-lookup"><span data-stu-id="ba47c-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba47c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba47c-115">Remarks</span></span>

<span data-ttu-id="ba47c-116">Это сообщение обычно используется для форматирования содержимого элемента управления Rich Edit для выходного устройства, такого как принтер.</span><span class="sxs-lookup"><span data-stu-id="ba47c-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="ba47c-117">После использования этого сообщения для форматирования диапазона текста важно освободить кэшированные данные, отправив **EM \_ форматранже** еще раз, но с параметром *lParam* , имеющим значение **null**. в противном случае произойдет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="ba47c-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="ba47c-118">Кроме того, после использования этого сообщения для одного устройства необходимо освободить кэшированные данные, прежде чем повторно использовать их для другого устройства.</span><span class="sxs-lookup"><span data-stu-id="ba47c-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba47c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ba47c-119">Requirements</span></span>



| <span data-ttu-id="ba47c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ba47c-120">Requirement</span></span> | <span data-ttu-id="ba47c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ba47c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba47c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba47c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba47c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba47c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba47c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba47c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba47c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba47c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba47c-126">Header</span><span class="sxs-lookup"><span data-stu-id="ba47c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba47c-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba47c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba47c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba47c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba47c-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ba47c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ba47c-130">**EM \_ дисплайбанд**</span><span class="sxs-lookup"><span data-stu-id="ba47c-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="ba47c-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ba47c-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ba47c-132">Печать элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="ba47c-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





