---
title: Различные константы платформы (Мсктф. h)
description: Различные константы платформы указывают параметры для клиентов, процессов или текста.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492315"
---
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="50194-103">Различные константы платформы</span><span class="sxs-lookup"><span data-stu-id="50194-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="50194-104">Различные константы платформы указывают параметры для клиентов, процессов или текста.</span><span class="sxs-lookup"><span data-stu-id="50194-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="50194-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="50194-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="50194-106">Описание</span><span class="sxs-lookup"><span data-stu-id="50194-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="50194-107"><dt>**Tf \_ CLIENTID \_ null**</dt> <dt>((тфклиентид) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="50194-108">Указывает на службу текстового ввода, которую клиент деактивирует.</span><span class="sxs-lookup"><span data-stu-id="50194-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="50194-109">См. [тфклиентид](tfclientid.md).</span><span class="sxs-lookup"><span data-stu-id="50194-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="50194-110"><dt>**Tf \_ Недопустимый \_ гуидатом**</dt> <dt>((тфгуидатом) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="50194-111">Недопустимое значение [тфгуидатом](tfguidatom.md) для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="50194-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="50194-112"><dt>**Tf \_ \_Выбор по умолчанию**</dt> <dt>(Выбор служб терминалов \_ по умолчанию \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="50194-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="50194-113">Использовать выбор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50194-113">Use the default selection.</span></span> <span data-ttu-id="50194-114">Используется [ITfContext:: SELECT](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)и [итекстстореанчор:: SELECT](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span><span class="sxs-lookup"><span data-stu-id="50194-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="50194-115"><dt>**Tf \_ ГТП, \_ включая \_ текст**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="50194-116">Указывает, что метод [итфедитрекорд:: жеттекстандпропертюпдатес](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) будет получать коллекцию объектов Range, охватывающую текст, измененный во время сеанса редактирования.</span><span class="sxs-lookup"><span data-stu-id="50194-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="50194-117"><dt>**Tf \_ \_Объект HF**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="50194-118">Если обнаружен внедренный объект, то при сдвиге диапазона останавливается.</span><span class="sxs-lookup"><span data-stu-id="50194-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="50194-119">Используется в **dwFlags** члене структуры [tf \_ халтконд](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .</span><span class="sxs-lookup"><span data-stu-id="50194-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="50194-120"><dt>**Tf \_ \_Исправление IE**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="50194-121">Текст представляет собой преобразование (исправление) существующего содержимого, чтобы другие текстовые службы могли сохранять данные, связанные с исходным текстом.</span><span class="sxs-lookup"><span data-stu-id="50194-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="50194-122">Используется в параметре *dwFlags* объекта [Итфранже:: инсертембеддед](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="50194-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="50194-123"><dt>**Tf \_ Недопустимый \_ файл cookie**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="50194-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="50194-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="50194-125"><dt>**Tf \_ НЕДОПУСТИМое \_ изменение \_ файла cookie**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="50194-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="50194-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="50194-127"><dt>**Tf \_ ПОПФ \_ все**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="50194-128">Все контексты удаляются из стека.</span><span class="sxs-lookup"><span data-stu-id="50194-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="50194-129">Используется в параметре *dwFlags* параметра [ITfDocumentMgr::P Op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span><span class="sxs-lookup"><span data-stu-id="50194-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="50194-130"><dt>**Tf \_ ST- \_ исправление**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="50194-131">Текст представляет собой преобразование (исправление) существующего содержимого, чтобы другие текстовые службы могли сохранять данные, связанные с исходным текстом.</span><span class="sxs-lookup"><span data-stu-id="50194-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="50194-132">Используется в параметре *dwFlags* объекта [Итфранже:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span><span class="sxs-lookup"><span data-stu-id="50194-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="50194-133"><dt>**Tf \_ \_Исправление Tu**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="50194-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="50194-134">Изменение текста является результатом преобразования (исправления) существующего содержимого.</span><span class="sxs-lookup"><span data-stu-id="50194-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="50194-135">Это означает, что семантика текста не изменилась.</span><span class="sxs-lookup"><span data-stu-id="50194-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="50194-136">Используется в параметре *dwFlags* объекта [Итфпропертисторе:: онтекступдатед](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span><span class="sxs-lookup"><span data-stu-id="50194-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="50194-137"><dt>**Tf \_ US \_ хидетипуи**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="50194-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="50194-138">Не используется.</span><span class="sxs-lookup"><span data-stu-id="50194-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="50194-139">Требования</span><span class="sxs-lookup"><span data-stu-id="50194-139">Requirements</span></span>



| <span data-ttu-id="50194-140">Требование</span><span class="sxs-lookup"><span data-stu-id="50194-140">Requirement</span></span> | <span data-ttu-id="50194-141">Значение</span><span class="sxs-lookup"><span data-stu-id="50194-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50194-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50194-142">Minimum supported client</span></span><br/> | <span data-ttu-id="50194-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50194-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="50194-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50194-144">Minimum supported server</span></span><br/> | <span data-ttu-id="50194-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50194-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="50194-146">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="50194-146">Redistributable</span></span><br/>          | <span data-ttu-id="50194-147">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="50194-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="50194-148">Header</span><span class="sxs-lookup"><span data-stu-id="50194-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="50194-149"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="50194-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="50194-150">IDL</span><span class="sxs-lookup"><span data-stu-id="50194-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50194-151"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50194-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50194-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50194-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50194-153">ITextStoreACP:: выделять</span><span class="sxs-lookup"><span data-stu-id="50194-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="50194-154">Итекстстореанчор:: выделять</span><span class="sxs-lookup"><span data-stu-id="50194-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="50194-155">ITfContext:: выделять</span><span class="sxs-lookup"><span data-stu-id="50194-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="50194-156">ITfDocumentMgr::P Op</span><span class="sxs-lookup"><span data-stu-id="50194-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="50194-157">Итфедитрекорд:: Жеттекстандпропертюпдатес</span><span class="sxs-lookup"><span data-stu-id="50194-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="50194-158">Итфпропертисторе:: Онтекступдатед</span><span class="sxs-lookup"><span data-stu-id="50194-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="50194-159">Итфранже:: Инсертембеддед</span><span class="sxs-lookup"><span data-stu-id="50194-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="50194-160">Итфранже:: SetText</span><span class="sxs-lookup"><span data-stu-id="50194-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="50194-161">тфклиентид</span><span class="sxs-lookup"><span data-stu-id="50194-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="50194-162">тфгуидатом</span><span class="sxs-lookup"><span data-stu-id="50194-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="50194-163">TF \_ халтконд</span><span class="sxs-lookup"><span data-stu-id="50194-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





