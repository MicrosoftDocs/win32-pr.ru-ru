---
title: Сообщение EM_STREAMIN (RichEdit. h)
description: Заменяет содержимое элемента управления Rich Edit потоком данных, предоставленным приложением, определенным в приложении \ 8211; Функция обратного вызова Едитстреамкаллбакк.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Элементы управления Windows для EM_STREAMIN сообщений
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492168"
---
# <a name="em_streamin-message"></a><span data-ttu-id="fddb9-104">\_Сообщение о потоке EM</span><span class="sxs-lookup"><span data-stu-id="fddb9-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="fddb9-105">Заменяет содержимое элемента управления Rich Edit потоком данных, предоставленным приложением, определенным функцией обратного вызова [*едитстреамкаллбакк*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) .</span><span class="sxs-lookup"><span data-stu-id="fddb9-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="fddb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fddb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fddb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fddb9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fddb9-108">Задает формат данных и параметры замены.</span><span class="sxs-lookup"><span data-stu-id="fddb9-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="fddb9-109">Это значение должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fddb9-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="fddb9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fddb9-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="fddb9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fddb9-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="fddb9-112"><dt>**SF \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb9-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="fddb9-113">RTF</span><span class="sxs-lookup"><span data-stu-id="fddb9-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="fddb9-114"><dt>**\_текст**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb9-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="fddb9-115">Текст</span><span class="sxs-lookup"><span data-stu-id="fddb9-115">Text</span></span><br/> |



 

<span data-ttu-id="fddb9-116">Кроме того, можно указать следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="fddb9-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="fddb9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fddb9-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="fddb9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fddb9-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="fddb9-119"><dt>**СФФ \_ плаинртф**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb9-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="fddb9-120">Если этот значение задано, в потоки передаются только ключевые слова, общие для всех языков.</span><span class="sxs-lookup"><span data-stu-id="fddb9-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="fddb9-121">В потоке ключевые слова RTF, относящиеся к определенному языку, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="fddb9-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="fddb9-122">Если не указано, то все ключевые слова помещаются в поток.</span><span class="sxs-lookup"><span data-stu-id="fddb9-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="fddb9-123">Этот флаг можно объединить с флагом **SF \_ RTF** .</span><span class="sxs-lookup"><span data-stu-id="fddb9-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="fddb9-124"><dt>**СФФ \_ Выбор**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb9-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="fddb9-125">Если этот параметр указан, поток данных заменяет содержимое текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="fddb9-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="fddb9-126">Если не указано, поток данных заменяет все содержимое элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fddb9-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="fddb9-127">Этот флаг можно объединить с флагами « **SF \_ » или** « **SF \_ RTF** ».</span><span class="sxs-lookup"><span data-stu-id="fddb9-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="fddb9-128"><dt>**SF \_ Юникод**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb9-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="fddb9-129">**Microsoft Rich Edit 2,0 и более поздние версии:** Указывает текст в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="fddb9-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="fddb9-130">Этот флаг можно объединить с флагом **\_ текста** .</span><span class="sxs-lookup"><span data-stu-id="fddb9-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="fddb9-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fddb9-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fddb9-132">Указатель на структуру [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="fddb9-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="fddb9-133">На входе **пфнкаллбакк** член этой структуры должен указывать на приложение, определенную [*едитстреамкаллбакк*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) функцию.</span><span class="sxs-lookup"><span data-stu-id="fddb9-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="fddb9-134">В выходных данных элемент **дверрор** может содержать ненулевой код ошибки, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fddb9-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fddb9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fddb9-135">Return value</span></span>

<span data-ttu-id="fddb9-136">Это сообщение возвращает число считанных символов.</span><span class="sxs-lookup"><span data-stu-id="fddb9-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="fddb9-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fddb9-137">Remarks</span></span>

<span data-ttu-id="fddb9-138">При отправке сообщения с большим объемом **EM \_** элемент управления Rich Edit выполняет повторные вызовы функции [*Едитстреамкаллбакк*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) , указанной элементом **пфнкаллбакк** структуры [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="fddb9-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="fddb9-139">При каждом вызове функции обратного вызова она заполняет буфер данными для чтения в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="fddb9-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="fddb9-140">Это происходит до тех пор, пока функция обратного вызова не указывает, что потоковая операция была завершена или произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fddb9-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="fddb9-141">Требования</span><span class="sxs-lookup"><span data-stu-id="fddb9-141">Requirements</span></span>



| <span data-ttu-id="fddb9-142">Требование</span><span class="sxs-lookup"><span data-stu-id="fddb9-142">Requirement</span></span> | <span data-ttu-id="fddb9-143">Значение</span><span class="sxs-lookup"><span data-stu-id="fddb9-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fddb9-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fddb9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="fddb9-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fddb9-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fddb9-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fddb9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="fddb9-147">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fddb9-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fddb9-148">Header</span><span class="sxs-lookup"><span data-stu-id="fddb9-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="fddb9-149"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fddb9-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fddb9-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fddb9-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="fddb9-151">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fddb9-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fddb9-152">**едитстреам**</span><span class="sxs-lookup"><span data-stu-id="fddb9-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="fddb9-153">*едитстреамкаллбакк*</span><span class="sxs-lookup"><span data-stu-id="fddb9-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="fddb9-154">**\_потоковая передача EM**</span><span class="sxs-lookup"><span data-stu-id="fddb9-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





