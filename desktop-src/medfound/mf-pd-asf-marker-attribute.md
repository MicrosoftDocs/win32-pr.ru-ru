---
description: Задает маркеры в файле расширенного формата систем (ASF). Этот атрибут соответствует объекту маркера в заголовке ASF, определенном в спецификации ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Атрибут MF_PD_ASF_MARKER (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684424"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="fd8bf-104">\_ \_ \_ Атрибут маркера MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="fd8bf-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="fd8bf-105">Задает маркеры в файле расширенного формата систем (ASF).</span><span class="sxs-lookup"><span data-stu-id="fd8bf-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="fd8bf-106">Этот атрибут соответствует объекту маркера в заголовке ASF, определенном в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd8bf-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fd8bf-107">Data type</span></span>

<span data-ttu-id="fd8bf-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="fd8bf-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8bf-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd8bf-109">Remarks</span></span>

<span data-ttu-id="fd8bf-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fd8bf-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из объекта маркера.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="fd8bf-112">В следующей таблице показан формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="fd8bf-113">Поле объекта маркера</span><span class="sxs-lookup"><span data-stu-id="fd8bf-113">Marker Object field</span></span> | <span data-ttu-id="fd8bf-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fd8bf-114">Data type</span></span>    | <span data-ttu-id="fd8bf-115">Размер</span><span class="sxs-lookup"><span data-stu-id="fd8bf-115">Size</span></span>    | <span data-ttu-id="fd8bf-116">Описание</span><span class="sxs-lookup"><span data-stu-id="fd8bf-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="fd8bf-117">Число маркеров</span><span class="sxs-lookup"><span data-stu-id="fd8bf-117">Markers Count</span></span>       | <span data-ttu-id="fd8bf-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-118">**DWORD**</span></span>    | <span data-ttu-id="fd8bf-119">4 байта</span><span class="sxs-lookup"><span data-stu-id="fd8bf-119">4 bytes</span></span> | <span data-ttu-id="fd8bf-120">Число маркеров</span><span class="sxs-lookup"><span data-stu-id="fd8bf-120">Number of markers</span></span> |
| <span data-ttu-id="fd8bf-121">Метки</span><span class="sxs-lookup"><span data-stu-id="fd8bf-121">Markers</span></span>             | <span data-ttu-id="fd8bf-122">**ДВУХБАЙТОВЫХ**\[\]</span><span class="sxs-lookup"><span data-stu-id="fd8bf-122">**BYTE**\[\]</span></span> | <span data-ttu-id="fd8bf-123">Различается</span><span class="sxs-lookup"><span data-stu-id="fd8bf-123">Varies</span></span>  | <span data-ttu-id="fd8bf-124">Массив маркеров</span><span class="sxs-lookup"><span data-stu-id="fd8bf-124">Array of markers</span></span>  |



 

<span data-ttu-id="fd8bf-125">Первый **DWORD** — это число маркеров, за которыми следует массив маркеров.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="fd8bf-126">Каждый маркер имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-126">Each marker has the following format:</span></span>



| <span data-ttu-id="fd8bf-127">Поле объекта маркера</span><span class="sxs-lookup"><span data-stu-id="fd8bf-127">Marker Object field</span></span>       | <span data-ttu-id="fd8bf-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fd8bf-128">Data type</span></span>     | <span data-ttu-id="fd8bf-129">Размер</span><span class="sxs-lookup"><span data-stu-id="fd8bf-129">Size</span></span>    | <span data-ttu-id="fd8bf-130">Описание</span><span class="sxs-lookup"><span data-stu-id="fd8bf-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-131">Длина описания маркера</span><span class="sxs-lookup"><span data-stu-id="fd8bf-131">Marker Description Length</span></span> | <span data-ttu-id="fd8bf-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-132">**DWORD**</span></span>     | <span data-ttu-id="fd8bf-133">4 байта</span><span class="sxs-lookup"><span data-stu-id="fd8bf-133">4 bytes</span></span> | <span data-ttu-id="fd8bf-134">Размер строки описания в байтах, включая символ NULL.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="fd8bf-135">Описание маркера</span><span class="sxs-lookup"><span data-stu-id="fd8bf-135">Marker Description</span></span>        | <span data-ttu-id="fd8bf-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="fd8bf-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="fd8bf-137">Различается</span><span class="sxs-lookup"><span data-stu-id="fd8bf-137">Varies</span></span>  | <span data-ttu-id="fd8bf-138">Строка, завершающаяся нулем, описывающая маркер.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="fd8bf-139">Время презентации</span><span class="sxs-lookup"><span data-stu-id="fd8bf-139">Presentation Time</span></span>         | <span data-ttu-id="fd8bf-140">**лонглонг**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-140">**LONGLONG**</span></span>  | <span data-ttu-id="fd8bf-141">8 байт</span><span class="sxs-lookup"><span data-stu-id="fd8bf-141">8 bytes</span></span> | <span data-ttu-id="fd8bf-142">Время представления маркера в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="fd8bf-143">Время отправки</span><span class="sxs-lookup"><span data-stu-id="fd8bf-143">Send Time</span></span>                 | <span data-ttu-id="fd8bf-144">**лонглонг**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-144">**LONGLONG**</span></span>  | <span data-ttu-id="fd8bf-145">8 байт</span><span class="sxs-lookup"><span data-stu-id="fd8bf-145">8 bytes</span></span> | <span data-ttu-id="fd8bf-146">Время отправки записи маркера в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="fd8bf-147">Offset</span><span class="sxs-lookup"><span data-stu-id="fd8bf-147">Offset</span></span>                    | <span data-ttu-id="fd8bf-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-148">**UINT64**</span></span>    | <span data-ttu-id="fd8bf-149">8 байт</span><span class="sxs-lookup"><span data-stu-id="fd8bf-149">8 bytes</span></span> | <span data-ttu-id="fd8bf-150">Смещение (в байтах) к объекту данных, который указывает расположение рынка.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="fd8bf-151">Требования</span><span class="sxs-lookup"><span data-stu-id="fd8bf-151">Requirements</span></span>



| <span data-ttu-id="fd8bf-152">Требование</span><span class="sxs-lookup"><span data-stu-id="fd8bf-152">Requirement</span></span> | <span data-ttu-id="fd8bf-153">Значение</span><span class="sxs-lookup"><span data-stu-id="fd8bf-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd8bf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="fd8bf-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd8bf-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fd8bf-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd8bf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="fd8bf-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd8bf-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd8bf-158">Header</span><span class="sxs-lookup"><span data-stu-id="fd8bf-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd8bf-159"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8bf-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8bf-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd8bf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8bf-161">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd8bf-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd8bf-162">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fd8bf-163">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fd8bf-164">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fd8bf-165">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="fd8bf-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd8bf-166">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="fd8bf-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="fd8bf-167">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="fd8bf-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




