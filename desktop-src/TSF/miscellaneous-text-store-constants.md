---
title: Прочие константы хранилища текста (Текстстор. h)
description: В прочих константах хранилища текста задаются определенные свойства для хранилищ текста.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137046"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="a7784-103">Прочие константы хранилища текста</span><span class="sxs-lookup"><span data-stu-id="a7784-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="a7784-104">В прочих константах хранилища текста задаются определенные свойства для хранилищ текста.</span><span class="sxs-lookup"><span data-stu-id="a7784-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="a7784-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="a7784-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="a7784-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a7784-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="a7784-107"><dt>**TS \_ \_Выбор по умолчанию**</dt> <dt>((ulong)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="a7784-108">Если для параметра *Улиндекс* [ITfContext::-SELECT](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) задано это значение, выбирается выбор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7784-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="a7784-109"><dt>**TS \_ ЖЕА \_ Hidden**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="a7784-110">Если  для параметра dwFlags [итекстстореанчор:: onembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) задано это значение, то внедренный объект может находиться в скрытом тексте.</span><span class="sxs-lookup"><span data-stu-id="a7784-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="a7784-111"><dt>**TS \_ ГТА \_ Hidden**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="a7784-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="a7784-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="a7784-113"><dt>**TS \_ ST- \_ исправление**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="a7784-114">Если  для параметра dwFlags [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [Итекстстореанчор:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)или [ITextStoreACPSink:: онтекстчанже](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) задано это значение, то текст представляет собой преобразование (исправление) существующего содержимого, а также все специальные сведения о текстовой разметке (метаданные), такие как данные файла WAV или идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="a7784-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="a7784-115"><dt>**TS \_ \_Коррекция TC**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="a7784-116">Если  для параметра dwFlags [Итекстстореанчорсинк:: онтекстчанже](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) задано это значение, то текст представляет собой преобразование (исправление) существующего содержимого, а также все специальные сведения о текстовой разметке (метаданные), такие как данные файла WAV или идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="a7784-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="a7784-117"><dt>**TS \_ ВКУКИЕ \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="a7784-118">Используется внутри TSF.</span><span class="sxs-lookup"><span data-stu-id="a7784-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="a7784-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a7784-119">Requirements</span></span>



| <span data-ttu-id="a7784-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a7784-120">Requirement</span></span> | <span data-ttu-id="a7784-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a7784-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7784-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7784-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7784-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a7784-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a7784-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7784-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7784-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a7784-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7784-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a7784-126">Redistributable</span></span><br/>          | <span data-ttu-id="a7784-127">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="a7784-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="a7784-128">Header</span><span class="sxs-lookup"><span data-stu-id="a7784-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7784-129"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7784-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a7784-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7784-131"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7784-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7784-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7784-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7784-133">ITfContext:: выделять</span><span class="sxs-lookup"><span data-stu-id="a7784-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="a7784-134">ITextStoreACP:: SetText</span><span class="sxs-lookup"><span data-stu-id="a7784-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="a7784-135">Итекстстореанчор:: SetText</span><span class="sxs-lookup"><span data-stu-id="a7784-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="a7784-136">Итекстстореанчор:: onembedded</span><span class="sxs-lookup"><span data-stu-id="a7784-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="a7784-137">ITextStoreACPSink:: Онтекстчанже</span><span class="sxs-lookup"><span data-stu-id="a7784-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="a7784-138">Итекстстореанчорсинк:: Онтекстчанже</span><span class="sxs-lookup"><span data-stu-id="a7784-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="a7784-139">Различные константы платформы</span><span class="sxs-lookup"><span data-stu-id="a7784-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





