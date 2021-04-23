---
description: Содержит список языков RFC 1766, используемых в текущей презентации.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Атрибут MF_PD_ASF_LANGLIST_LEGACYORDER (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683875"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="5e629-103">\_ \_ \_ \_ Атрибут ланглист легациордер для MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="5e629-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="5e629-104">Содержит список языков RFC 1766, используемых в текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="5e629-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e629-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5e629-105">Data type</span></span>

<span data-ttu-id="5e629-106">**ДВУХБАЙТОВЫХ \[\]**</span><span class="sxs-lookup"><span data-stu-id="5e629-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="5e629-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="5e629-107">Get/set</span></span>

<span data-ttu-id="5e629-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="5e629-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="5e629-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="5e629-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5e629-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="5e629-110">Applies to</span></span>

[<span data-ttu-id="5e629-111">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="5e629-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="5e629-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e629-112">Remarks</span></span>

<span data-ttu-id="5e629-113">Этот атрибут применяется к дескрипторам представления, созданным из [объекта ASF контентинфо](asf-contentinfo-object.md) с помощью вызова [**Имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="5e629-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="5e629-114">Формат массива байтов выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5e629-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="5e629-115">Поле объекта списка языков</span><span class="sxs-lookup"><span data-stu-id="5e629-115">Language List Object field</span></span> | <span data-ttu-id="5e629-116">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5e629-116">Data type</span></span>    | <span data-ttu-id="5e629-117">Размер</span><span class="sxs-lookup"><span data-stu-id="5e629-117">Size</span></span>    | <span data-ttu-id="5e629-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5e629-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="5e629-119">Число записей ИДЕНТИФИКАТОРов языков</span><span class="sxs-lookup"><span data-stu-id="5e629-119">Language ID Records Count</span></span>  | <span data-ttu-id="5e629-120">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="5e629-120">**DWORD**</span></span>    | <span data-ttu-id="5e629-121">4 байта</span><span class="sxs-lookup"><span data-stu-id="5e629-121">4 bytes</span></span> | <span data-ttu-id="5e629-122">Число языков</span><span class="sxs-lookup"><span data-stu-id="5e629-122">Number of languages</span></span>                    |
| <span data-ttu-id="5e629-123">Записи идентификатора языка</span><span class="sxs-lookup"><span data-stu-id="5e629-123">Language ID Records</span></span>        | <span data-ttu-id="5e629-124">**ДВУХБАЙТОВЫХ**\[\]</span><span class="sxs-lookup"><span data-stu-id="5e629-124">**BYTE**\[\]</span></span> | <span data-ttu-id="5e629-125">Различается</span><span class="sxs-lookup"><span data-stu-id="5e629-125">Varies</span></span>  | <span data-ttu-id="5e629-126">Массив строк языка (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="5e629-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="5e629-127">Первый **DWORD** — это число языков, за которым следует массив строк идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="5e629-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="5e629-128">Каждая строка имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="5e629-128">Each string has the following format:</span></span>



| <span data-ttu-id="5e629-129">Поле объекта списка языков</span><span class="sxs-lookup"><span data-stu-id="5e629-129">Language List Object field</span></span> | <span data-ttu-id="5e629-130">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5e629-130">Data type</span></span>     | <span data-ttu-id="5e629-131">Размер</span><span class="sxs-lookup"><span data-stu-id="5e629-131">Size</span></span>    | <span data-ttu-id="5e629-132">Описание</span><span class="sxs-lookup"><span data-stu-id="5e629-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e629-133">Длина идентификатора языка</span><span class="sxs-lookup"><span data-stu-id="5e629-133">Language ID Length</span></span>         | <span data-ttu-id="5e629-134">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="5e629-134">**DWORD**</span></span>     | <span data-ttu-id="5e629-135">4 байта</span><span class="sxs-lookup"><span data-stu-id="5e629-135">4 bytes</span></span> | <span data-ttu-id="5e629-136">Длина строки в байтах, включая размер завершающего **нуль** символа.</span><span class="sxs-lookup"><span data-stu-id="5e629-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="5e629-137">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="5e629-137">Language ID</span></span>                | <span data-ttu-id="5e629-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="5e629-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="5e629-139">Различается</span><span class="sxs-lookup"><span data-stu-id="5e629-139">Varies</span></span>  | <span data-ttu-id="5e629-140">Строка, заканчивающаяся нулем и содержащая имя языка RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="5e629-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="5e629-141">Каждая строка является тегом языка, совместимым с RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="5e629-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="5e629-142">Используйте этот атрибут только для обеспечения обратной совместимости с порядком перечисления интерфейса [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5e629-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="5e629-143">Строки языка хранятся в атрибуте [**MF \_ PD \_ ASF \_ ланглист**](mf-pd-asf-langlist-attribute.md) в другом порядке.</span><span class="sxs-lookup"><span data-stu-id="5e629-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e629-144">Требования</span><span class="sxs-lookup"><span data-stu-id="5e629-144">Requirements</span></span>



| <span data-ttu-id="5e629-145">Требование</span><span class="sxs-lookup"><span data-stu-id="5e629-145">Requirement</span></span> | <span data-ttu-id="5e629-146">Значение</span><span class="sxs-lookup"><span data-stu-id="5e629-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e629-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e629-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5e629-148">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5e629-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e629-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e629-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5e629-150">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e629-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e629-151">Header</span><span class="sxs-lookup"><span data-stu-id="5e629-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e629-152"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e629-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e629-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e629-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e629-154">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e629-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e629-155">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="5e629-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
