---
description: Указывает язык, используемый потоком в файле ASF.
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: Атрибут MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647453"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="cc19e-103">\_Индекс MF SD \_ ASF \_ екстстрмпроп \_ Language \_ ID \_ атрибут</span><span class="sxs-lookup"><span data-stu-id="cc19e-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="cc19e-104">Указывает язык, используемый потоком в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="cc19e-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="cc19e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc19e-105">Data type</span></span>

<span data-ttu-id="cc19e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cc19e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cc19e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc19e-107">Remarks</span></span>

<span data-ttu-id="cc19e-108">Этот атрибут применяется к дескрипторам потоков для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="cc19e-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="cc19e-109">Это значение является индексом в списке языков, который содержится в атрибуте [**\_ \_ \_ ланглист MF PD ASF**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="cc19e-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="cc19e-110">Этот атрибут соответствует полю индекса идентификатора языка потока в объекте свойств расширенного потока.</span><span class="sxs-lookup"><span data-stu-id="cc19e-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="cc19e-111">Дополнительные сведения см. в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="cc19e-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="cc19e-112">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="cc19e-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="cc19e-113">Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="cc19e-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="cc19e-114">Можно также получить тег Language, запросив дескриптор потока для атрибута [**MF \_ \_ языка SD**](mf-sd-language-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="cc19e-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc19e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cc19e-115">Requirements</span></span>



| <span data-ttu-id="cc19e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cc19e-116">Requirement</span></span> | <span data-ttu-id="cc19e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cc19e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc19e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc19e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc19e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc19e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc19e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc19e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc19e-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc19e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cc19e-122">Header</span><span class="sxs-lookup"><span data-stu-id="cc19e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc19e-123"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc19e-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc19e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc19e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc19e-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc19e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc19e-126">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="cc19e-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cc19e-127">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="cc19e-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="cc19e-128">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="cc19e-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="cc19e-129">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="cc19e-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc19e-130">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="cc19e-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




