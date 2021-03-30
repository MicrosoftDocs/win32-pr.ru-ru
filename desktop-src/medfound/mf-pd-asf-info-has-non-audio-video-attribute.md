---
description: Указывает, содержит ли ASF-файл любые потоки, не являющиеся звуком или видео.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: Атрибут MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998951"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="73bf4-103">MF \_ PD \_ ASF \_ сведения \_ имеет \_ \_ атрибут неаудио \_ видео</span><span class="sxs-lookup"><span data-stu-id="73bf4-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="73bf4-104">Указывает, содержит ли ASF-файл любые потоки, не являющиеся звуком или видео.</span><span class="sxs-lookup"><span data-stu-id="73bf4-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="73bf4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="73bf4-105">Data type</span></span>

<span data-ttu-id="73bf4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73bf4-106">**UINT32**</span></span>

<span data-ttu-id="73bf4-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="73bf4-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73bf4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73bf4-108">Remarks</span></span>

<span data-ttu-id="73bf4-109">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="73bf4-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="73bf4-110">Если значение равно **true**, файл содержит по крайней мере один поток, который не является звуком или видео.</span><span class="sxs-lookup"><span data-stu-id="73bf4-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="73bf4-111">К примерам относятся потоки изображений, команды сценариев и пользовательские произвольные данные.</span><span class="sxs-lookup"><span data-stu-id="73bf4-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="73bf4-112">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="73bf4-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="73bf4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="73bf4-113">Requirements</span></span>



| <span data-ttu-id="73bf4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="73bf4-114">Requirement</span></span> | <span data-ttu-id="73bf4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="73bf4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73bf4-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73bf4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="73bf4-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73bf4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="73bf4-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73bf4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="73bf4-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73bf4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="73bf4-120">Header</span><span class="sxs-lookup"><span data-stu-id="73bf4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="73bf4-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="73bf4-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73bf4-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73bf4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bf4-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73bf4-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73bf4-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="73bf4-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="73bf4-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73bf4-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="73bf4-126">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="73bf4-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="73bf4-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="73bf4-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="73bf4-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="73bf4-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




