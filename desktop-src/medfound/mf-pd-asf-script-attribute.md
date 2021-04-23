---
description: Указывает список команд сценария и параметры для файла ASF. Этот атрибут соответствует объекту команды скрипта в заголовке ASF, определенном в спецификации ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Атрибут MF_PD_ASF_SCRIPT (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712327"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="7987c-104">\_ \_ \_ Атрибут скрипта MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="7987c-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="7987c-105">Указывает список команд сценария и параметры для файла ASF.</span><span class="sxs-lookup"><span data-stu-id="7987c-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7987c-106">Этот атрибут соответствует объекту команды скрипта в заголовке ASF, определенном в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="7987c-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="7987c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7987c-107">Data type</span></span>

<span data-ttu-id="7987c-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="7987c-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="7987c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7987c-109">Remarks</span></span>

<span data-ttu-id="7987c-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="7987c-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="7987c-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из заголовка объекта команды скрипта.</span><span class="sxs-lookup"><span data-stu-id="7987c-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="7987c-112">В следующей таблице показан формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="7987c-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="7987c-113">Поле объекта команды сценария</span><span class="sxs-lookup"><span data-stu-id="7987c-113">Script Command Object field</span></span> | <span data-ttu-id="7987c-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7987c-114">Data type</span></span>    | <span data-ttu-id="7987c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="7987c-115">Size</span></span>    | <span data-ttu-id="7987c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7987c-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="7987c-117">Число команд</span><span class="sxs-lookup"><span data-stu-id="7987c-117">Commands Count</span></span>              | <span data-ttu-id="7987c-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7987c-118">**DWORD**</span></span>    | <span data-ttu-id="7987c-119">4 байта</span><span class="sxs-lookup"><span data-stu-id="7987c-119">4 bytes</span></span> | <span data-ttu-id="7987c-120">Число команд сценария</span><span class="sxs-lookup"><span data-stu-id="7987c-120">Number of script commands</span></span> |
| <span data-ttu-id="7987c-121">Тип команды, команды</span><span class="sxs-lookup"><span data-stu-id="7987c-121">Command Type, Commands</span></span>      | <span data-ttu-id="7987c-122">**ДВУХБАЙТОВЫХ**\[\]</span><span class="sxs-lookup"><span data-stu-id="7987c-122">**BYTE**\[\]</span></span> | <span data-ttu-id="7987c-123">Различается</span><span class="sxs-lookup"><span data-stu-id="7987c-123">Varies</span></span>  | <span data-ttu-id="7987c-124">Массив команд сценария</span><span class="sxs-lookup"><span data-stu-id="7987c-124">Array of script commands</span></span>  |



 

<span data-ttu-id="7987c-125">Первый **DWORD** — число команд сценария, за которыми следует массив команд.</span><span class="sxs-lookup"><span data-stu-id="7987c-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="7987c-126">Каждая команда сценария имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="7987c-126">Each script command has the following format:</span></span>



| <span data-ttu-id="7987c-127">Поле объекта команды сценария</span><span class="sxs-lookup"><span data-stu-id="7987c-127">Script Command Object field</span></span> | <span data-ttu-id="7987c-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7987c-128">Data type</span></span>     | <span data-ttu-id="7987c-129">Размер</span><span class="sxs-lookup"><span data-stu-id="7987c-129">Size</span></span>    | <span data-ttu-id="7987c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="7987c-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="7987c-131">Длина имени команды</span><span class="sxs-lookup"><span data-stu-id="7987c-131">Command Name Length</span></span>         | <span data-ttu-id="7987c-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7987c-132">**DWORD**</span></span>     | <span data-ttu-id="7987c-133">4 байта</span><span class="sxs-lookup"><span data-stu-id="7987c-133">4 bytes</span></span> | <span data-ttu-id="7987c-134">Размер строки команды в байтах, включая символ NULL.</span><span class="sxs-lookup"><span data-stu-id="7987c-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="7987c-135">Имя команды</span><span class="sxs-lookup"><span data-stu-id="7987c-135">Command Name</span></span>                | <span data-ttu-id="7987c-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="7987c-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="7987c-137">Различается</span><span class="sxs-lookup"><span data-stu-id="7987c-137">Varies</span></span>  | <span data-ttu-id="7987c-138">Строка, завершающаяся нулем, которая содержит команду скрипта.</span><span class="sxs-lookup"><span data-stu-id="7987c-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="7987c-139">Длина имени типа команды</span><span class="sxs-lookup"><span data-stu-id="7987c-139">Command Type Name Length</span></span>    | <span data-ttu-id="7987c-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7987c-140">**DWORD**</span></span>     | <span data-ttu-id="7987c-141">4 байта</span><span class="sxs-lookup"><span data-stu-id="7987c-141">4 bytes</span></span> | <span data-ttu-id="7987c-142">Размер строки типа команды в байтах, включая символ NULL.</span><span class="sxs-lookup"><span data-stu-id="7987c-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="7987c-143">Имя типа команды</span><span class="sxs-lookup"><span data-stu-id="7987c-143">Command Type Name</span></span>           | <span data-ttu-id="7987c-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="7987c-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="7987c-145">Различается</span><span class="sxs-lookup"><span data-stu-id="7987c-145">Varies</span></span>  | <span data-ttu-id="7987c-146">Строка, завершающаяся нулем, которая содержит тип команды.</span><span class="sxs-lookup"><span data-stu-id="7987c-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="7987c-147">Время презентации</span><span class="sxs-lookup"><span data-stu-id="7987c-147">Presentation Time</span></span>           | <span data-ttu-id="7987c-148">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7987c-148">**DWORD**</span></span>     | <span data-ttu-id="7987c-149">4 байта</span><span class="sxs-lookup"><span data-stu-id="7987c-149">4 bytes</span></span> | <span data-ttu-id="7987c-150">Время презентации команды в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="7987c-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="7987c-151">Требования</span><span class="sxs-lookup"><span data-stu-id="7987c-151">Requirements</span></span>



| <span data-ttu-id="7987c-152">Требование</span><span class="sxs-lookup"><span data-stu-id="7987c-152">Requirement</span></span> | <span data-ttu-id="7987c-153">Значение</span><span class="sxs-lookup"><span data-stu-id="7987c-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7987c-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7987c-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7987c-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7987c-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7987c-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7987c-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7987c-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7987c-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7987c-158">Header</span><span class="sxs-lookup"><span data-stu-id="7987c-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="7987c-159"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="7987c-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7987c-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7987c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7987c-161">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7987c-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7987c-162">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="7987c-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7987c-163">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="7987c-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7987c-164">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="7987c-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="7987c-165">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="7987c-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="7987c-166">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="7987c-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="7987c-167">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="7987c-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




