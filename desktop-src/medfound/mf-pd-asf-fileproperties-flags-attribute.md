---
description: Указывает, является ли файл ASF-файла широковещательным или недоступным для поиска. Это значение соответствует полю flags объекта свойств файла, определенному в спецификации ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Атрибут MF_PD_ASF_FILEPROPERTIES_FLAGS (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656644"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="fed8c-104">\_ \_ \_ \_ Атрибут флагов филепропертиес MF для ASF</span><span class="sxs-lookup"><span data-stu-id="fed8c-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="fed8c-105">Указывает, является ли файл ASF-файла широковещательным или недоступным для поиска.</span><span class="sxs-lookup"><span data-stu-id="fed8c-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="fed8c-106">Это значение соответствует полю flags объекта свойств файла, определенному в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="fed8c-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="fed8c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fed8c-107">Data type</span></span>

<span data-ttu-id="fed8c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fed8c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fed8c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fed8c-109">Remarks</span></span>

<span data-ttu-id="fed8c-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="fed8c-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="fed8c-111">Значение атрибута является побитовым оператором или для следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="fed8c-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="fed8c-112">Flag</span><span class="sxs-lookup"><span data-stu-id="fed8c-112">Flag</span></span> | <span data-ttu-id="fed8c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="fed8c-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed8c-114">0x01</span><span class="sxs-lookup"><span data-stu-id="fed8c-114">0x01</span></span> | <span data-ttu-id="fed8c-115">Флаг вещания.</span><span class="sxs-lookup"><span data-stu-id="fed8c-115">Broadcast flag.</span></span> <span data-ttu-id="fed8c-116">Файл находится в процессе создания.</span><span class="sxs-lookup"><span data-stu-id="fed8c-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="fed8c-117">0x02</span><span class="sxs-lookup"><span data-stu-id="fed8c-117">0x02</span></span> | <span data-ttu-id="fed8c-118">Флаг с возможностью поиска.</span><span class="sxs-lookup"><span data-stu-id="fed8c-118">Seekable flag.</span></span> <span data-ttu-id="fed8c-119">Файл доступен для поиска.</span><span class="sxs-lookup"><span data-stu-id="fed8c-119">The file is seekable.</span></span><br/> <span data-ttu-id="fed8c-120">Файл доступен для поиска, если имеется звуковой поток, а максимальный размер пакета данных равен минимальному размеру пакета данных.</span><span class="sxs-lookup"><span data-stu-id="fed8c-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="fed8c-121">Он также может быть доступен для поиска, если файл содержит аудиопоток и видеопоток с соответствующим простым объектом index.</span><span class="sxs-lookup"><span data-stu-id="fed8c-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="fed8c-122">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="fed8c-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="fed8c-123">Если установлен флаг вещания, следующие атрибуты в дескрипторе представления недопустимы:</span><span class="sxs-lookup"><span data-stu-id="fed8c-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="fed8c-124">**MF \_ PD \_ ASF \_ филепропертиес \_ File \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fed8c-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="fed8c-125">**\_ \_ \_ \_ время создания филепропертиес MF PD \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="fed8c-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="fed8c-126">**\_пакеты MF PD \_ ASF \_ филепропертиес \_**</span><span class="sxs-lookup"><span data-stu-id="fed8c-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="fed8c-127">**\_ \_ \_ длительность воспроизведения MF филепропертиес \_ ASF \_**</span><span class="sxs-lookup"><span data-stu-id="fed8c-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="fed8c-128">**\_период отправки MF PD \_ ASF \_ филепропертиес \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fed8c-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="fed8c-129">Кроме того, в атрибуте [**\_ \_ \_ Филепропертиес \_ максимального \_ \_ размера пакета MF**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) и MF, ASF, [**\_ \_ \_ филепропертиес \_ min \_ \_ PD**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) , в качестве значений атрибутов устанавливается фактический размер пакета.</span><span class="sxs-lookup"><span data-stu-id="fed8c-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed8c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="fed8c-130">Requirements</span></span>



| <span data-ttu-id="fed8c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="fed8c-131">Requirement</span></span> | <span data-ttu-id="fed8c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="fed8c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed8c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fed8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fed8c-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fed8c-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fed8c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fed8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fed8c-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fed8c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fed8c-137">Header</span><span class="sxs-lookup"><span data-stu-id="fed8c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed8c-138"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="fed8c-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed8c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fed8c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed8c-140">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fed8c-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fed8c-141">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="fed8c-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="fed8c-142">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fed8c-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="fed8c-143">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="fed8c-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fed8c-144">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="fed8c-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fed8c-145">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="fed8c-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="fed8c-146">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="fed8c-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




