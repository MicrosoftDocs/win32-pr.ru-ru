---
title: Константы TS_IE_ (Текстстор. h)
description: '\_Константы служб терминалов IE \_ \ описывают, как вставить текст, который может содержать внедренные объекты, используемые текстовыми службами.'
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135515"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="78c79-103">\_Константы служб терминалов IE \_ \*</span><span class="sxs-lookup"><span data-stu-id="78c79-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="78c79-104">\_Константы служб терминалов IE \_ \* описывают, как вставить текст, который может содержать внедренные объекты, используемые текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="78c79-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="78c79-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="78c79-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="78c79-106">Описание</span><span class="sxs-lookup"><span data-stu-id="78c79-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="78c79-107"><dt>**TS \_ \_Исправление IE**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="78c79-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="78c79-108">Текст представляет собой преобразование (исправление) существующего содержимого, а также все специальные сведения о разметке текста (метаданные), такие как WAV-файлы или идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="78c79-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="78c79-109"><dt>**TS \_ \_Композиция IE**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="78c79-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="78c79-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="78c79-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="78c79-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78c79-111">Remarks</span></span>

<span data-ttu-id="78c79-112">Эти константы используются в параметре *DwFlags* [ITextStoreACP:: инсертембеддед](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) и [итекстстореанчор:: инсертембеддед](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="78c79-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="78c79-113">Требования</span><span class="sxs-lookup"><span data-stu-id="78c79-113">Requirements</span></span>



| <span data-ttu-id="78c79-114">Требование</span><span class="sxs-lookup"><span data-stu-id="78c79-114">Requirement</span></span> | <span data-ttu-id="78c79-115">Значение</span><span class="sxs-lookup"><span data-stu-id="78c79-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c79-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78c79-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78c79-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="78c79-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="78c79-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78c79-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78c79-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="78c79-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78c79-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="78c79-120">Redistributable</span></span><br/>          | <span data-ttu-id="78c79-121">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="78c79-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="78c79-122">Header</span><span class="sxs-lookup"><span data-stu-id="78c79-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78c79-123"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c79-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="78c79-124">IDL</span><span class="sxs-lookup"><span data-stu-id="78c79-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78c79-125"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78c79-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c79-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78c79-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c79-127">ITextStoreACP:: Инсертембеддед</span><span class="sxs-lookup"><span data-stu-id="78c79-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="78c79-128">Итекстстореанчор:: Инсертембеддед</span><span class="sxs-lookup"><span data-stu-id="78c79-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





