---
description: Содержит сведения о кодеках и форматах, которые использовались для кодирования содержимого в формате ASF. Этот атрибут соответствует объекту списка кодеков в заголовке ASF, определенном в спецификации ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Атрибут MF_PD_ASF_CODECLIST (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693430"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="54128-104">\_ \_ Атрибут кодеклист MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="54128-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="54128-105">Содержит сведения о кодеках и форматах, которые использовались для кодирования содержимого в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="54128-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="54128-106">Этот атрибут соответствует объекту списка кодеков в заголовке ASF, определенном в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="54128-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="54128-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="54128-107">Data type</span></span>

<span data-ttu-id="54128-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="54128-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="54128-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54128-109">Remarks</span></span>

<span data-ttu-id="54128-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="54128-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="54128-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из объекта списка кодеков в заголовке ASF.</span><span class="sxs-lookup"><span data-stu-id="54128-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="54128-112">Приложение, использующее [источник мультимедиа ASF](asf-media-source.md) , может получить этот атрибут путем вызова [**Имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) и получения атрибута из дескриптора представления.</span><span class="sxs-lookup"><span data-stu-id="54128-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="54128-113">В следующей таблице показана структура большого двоичного объекта атрибута.</span><span class="sxs-lookup"><span data-stu-id="54128-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="54128-114">Поле объекта списка кодеков</span><span class="sxs-lookup"><span data-stu-id="54128-114">Codec List Object field</span></span> | <span data-ttu-id="54128-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="54128-115">Data type</span></span>    | <span data-ttu-id="54128-116">Размер</span><span class="sxs-lookup"><span data-stu-id="54128-116">Size</span></span>    | <span data-ttu-id="54128-117">Описание</span><span class="sxs-lookup"><span data-stu-id="54128-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="54128-118">Число записей кодека</span><span class="sxs-lookup"><span data-stu-id="54128-118">Codec Entries Count</span></span>     | <span data-ttu-id="54128-119">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="54128-119">**DWORD**</span></span>    | <span data-ttu-id="54128-120">4 байта</span><span class="sxs-lookup"><span data-stu-id="54128-120">4 bytes</span></span> | <span data-ttu-id="54128-121">Число кодеков</span><span class="sxs-lookup"><span data-stu-id="54128-121">Number of codecs</span></span>                      |
| <span data-ttu-id="54128-122">Записи кодека</span><span class="sxs-lookup"><span data-stu-id="54128-122">Codec Entries</span></span>           | <span data-ttu-id="54128-123">**ДВУХБАЙТОВЫХ**\[\]</span><span class="sxs-lookup"><span data-stu-id="54128-123">**BYTE**\[\]</span></span> | <span data-ttu-id="54128-124">Различается</span><span class="sxs-lookup"><span data-stu-id="54128-124">Varies</span></span>  | <span data-ttu-id="54128-125">Массив информационных структур кодеков</span><span class="sxs-lookup"><span data-stu-id="54128-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="54128-126">Поле "записи кода" представляет собой массив структур.</span><span class="sxs-lookup"><span data-stu-id="54128-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="54128-127">В следующей таблице показан формат каждой записи.</span><span class="sxs-lookup"><span data-stu-id="54128-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54128-128">Поле объекта списка кодеков</span><span class="sxs-lookup"><span data-stu-id="54128-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="54128-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="54128-129">Data type</span></span></th>
<th><span data-ttu-id="54128-130">Размер</span><span class="sxs-lookup"><span data-stu-id="54128-130">Size</span></span></th>
<th><span data-ttu-id="54128-131">Описание</span><span class="sxs-lookup"><span data-stu-id="54128-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54128-132">Тип</span><span class="sxs-lookup"><span data-stu-id="54128-132">Type</span></span></td>
<td><span data-ttu-id="54128-133"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="54128-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="54128-134">4 байта</span><span class="sxs-lookup"><span data-stu-id="54128-134">4 bytes</span></span></td>
<td><span data-ttu-id="54128-135">Тип кодека.</span><span class="sxs-lookup"><span data-stu-id="54128-135">Codec type.</span></span> <span data-ttu-id="54128-136">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="54128-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="54128-137">0x0001: аудиокодек</span><span class="sxs-lookup"><span data-stu-id="54128-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="54128-138">0x0002: видеокодек</span><span class="sxs-lookup"><span data-stu-id="54128-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="54128-139">0xFFFF: неизвестно</span><span class="sxs-lookup"><span data-stu-id="54128-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54128-140">Длина имени кодека</span><span class="sxs-lookup"><span data-stu-id="54128-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="54128-141"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="54128-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="54128-142">4 байта</span><span class="sxs-lookup"><span data-stu-id="54128-142">4 bytes</span></span></td>
<td><span data-ttu-id="54128-143">Размер строки имени кодека в байтах, включая символ <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="54128-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54128-144">Имя кодека</span><span class="sxs-lookup"><span data-stu-id="54128-144">Codec Name</span></span></td>
<td><span data-ttu-id="54128-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="54128-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="54128-146">Различается</span><span class="sxs-lookup"><span data-stu-id="54128-146">Varies</span></span></td>
<td><span data-ttu-id="54128-147">Строка Юникода, заканчивающаяся нулем, которая содержит имя кодека, например &quot; Windows Media Video 9 &quot; .</span><span class="sxs-lookup"><span data-stu-id="54128-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54128-148">Длина описания кодека</span><span class="sxs-lookup"><span data-stu-id="54128-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="54128-149"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="54128-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="54128-150">4 байта</span><span class="sxs-lookup"><span data-stu-id="54128-150">4 bytes</span></span></td>
<td><span data-ttu-id="54128-151">Размер строки описания кодека в байтах, включая символ <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="54128-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54128-152">Описание кодека</span><span class="sxs-lookup"><span data-stu-id="54128-152">Codec Description</span></span></td>
<td><span data-ttu-id="54128-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="54128-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="54128-154">Различается</span><span class="sxs-lookup"><span data-stu-id="54128-154">Varies</span></span></td>
<td><span data-ttu-id="54128-155">Строка в Юникоде, заканчивающаяся нулем и содержащая описание кодека.</span><span class="sxs-lookup"><span data-stu-id="54128-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54128-156">Длина сведений о кодека</span><span class="sxs-lookup"><span data-stu-id="54128-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="54128-157"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="54128-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="54128-158">4 байта</span><span class="sxs-lookup"><span data-stu-id="54128-158">4 bytes</span></span></td>
<td><span data-ttu-id="54128-159">Размер поля сведений кодека в байтах.</span><span class="sxs-lookup"><span data-stu-id="54128-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54128-160">Сведения о кодека</span><span class="sxs-lookup"><span data-stu-id="54128-160">Codec Information</span></span></td>
<td><span data-ttu-id="54128-161"><strong>Byte</strong>[]</span><span class="sxs-lookup"><span data-stu-id="54128-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="54128-162">Различается</span><span class="sxs-lookup"><span data-stu-id="54128-162">Varies</span></span></td>
<td><span data-ttu-id="54128-163">Данные кодека.</span><span class="sxs-lookup"><span data-stu-id="54128-163">Codec data.</span></span> <span data-ttu-id="54128-164">Значение этих данных зависит от кодека.</span><span class="sxs-lookup"><span data-stu-id="54128-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="54128-165">Как правило, эти данные обозначают формат.</span><span class="sxs-lookup"><span data-stu-id="54128-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="54128-166">Макет большого двоичного объекта атрибута не точно соответствует макету объекта списка кодеков в заголовке ASF.</span><span class="sxs-lookup"><span data-stu-id="54128-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="54128-167">В частности, длины строк задаются в байтах и включают размер терминатора **null** .</span><span class="sxs-lookup"><span data-stu-id="54128-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54128-168">Требования</span><span class="sxs-lookup"><span data-stu-id="54128-168">Requirements</span></span>



| <span data-ttu-id="54128-169">Требование</span><span class="sxs-lookup"><span data-stu-id="54128-169">Requirement</span></span> | <span data-ttu-id="54128-170">Значение</span><span class="sxs-lookup"><span data-stu-id="54128-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54128-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54128-171">Minimum supported client</span></span><br/> | <span data-ttu-id="54128-172">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54128-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54128-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54128-173">Minimum supported server</span></span><br/> | <span data-ttu-id="54128-174">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54128-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="54128-175">Header</span><span class="sxs-lookup"><span data-stu-id="54128-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="54128-176"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="54128-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54128-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54128-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54128-178">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54128-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="54128-179">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="54128-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="54128-180">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="54128-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="54128-181">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="54128-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="54128-182">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="54128-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="54128-183">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="54128-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="54128-184">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="54128-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




