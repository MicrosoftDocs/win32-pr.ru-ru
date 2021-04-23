---
description: Указывает, содержит ли файл ASF (Расширенный системный формат) по крайней мере один видеопоток.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: Атрибут MF_PD_ASF_INFO_HAS_VIDEO (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712400"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="c6643-103">MF \_ PD \_ ASF \_ сведения \_ имеют \_ атрибут Video</span><span class="sxs-lookup"><span data-stu-id="c6643-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="c6643-104">Указывает, содержит ли файл ASF (Расширенный системный формат) по крайней мере один видеопоток.</span><span class="sxs-lookup"><span data-stu-id="c6643-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6643-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c6643-105">Data type</span></span>

<span data-ttu-id="c6643-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6643-106">**UINT32**</span></span>

<span data-ttu-id="c6643-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="c6643-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6643-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6643-108">Remarks</span></span>

<span data-ttu-id="c6643-109">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="c6643-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="c6643-110">Если значение равно **true**, файл содержит по крайней мере один видеопоток.</span><span class="sxs-lookup"><span data-stu-id="c6643-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="c6643-111">В противном случае файл не содержит потоков видео.</span><span class="sxs-lookup"><span data-stu-id="c6643-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="c6643-112">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="c6643-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6643-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c6643-113">Requirements</span></span>



| <span data-ttu-id="c6643-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c6643-114">Requirement</span></span> | <span data-ttu-id="c6643-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c6643-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6643-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6643-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6643-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6643-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c6643-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6643-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6643-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6643-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c6643-120">Header</span><span class="sxs-lookup"><span data-stu-id="c6643-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6643-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6643-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6643-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6643-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6643-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6643-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6643-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6643-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c6643-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c6643-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c6643-126">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="c6643-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c6643-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="c6643-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6643-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="c6643-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




