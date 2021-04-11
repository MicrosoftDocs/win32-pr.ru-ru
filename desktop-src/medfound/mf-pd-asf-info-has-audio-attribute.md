---
description: Указывает, содержит ли файл ASF какие-либо звуковые потоки.
ms.assetid: b7c5cd67-fd2a-49d8-8de5-61783a3b4577
title: Атрибут MF_PD_ASF_INFO_HAS_AUDIO (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e2fbf9698e470af92cbd21fc5f26883dc5fd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265506"
---
# <a name="mf_pd_asf_info_has_audio-attribute"></a><span data-ttu-id="aa5e6-103">MF \_ PD \_ ASF \_ info \_ имеет \_ атрибут Audio</span><span class="sxs-lookup"><span data-stu-id="aa5e6-103">MF\_PD\_ASF\_INFO\_HAS\_AUDIO attribute</span></span>

<span data-ttu-id="aa5e6-104">Указывает, содержит ли файл ASF какие-либо звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-104">Specifies whether an Advanced Systems Format (ASF) file contains any audio streams.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa5e6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aa5e6-105">Data type</span></span>

<span data-ttu-id="aa5e6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="aa5e6-106">**UINT32**</span></span>

<span data-ttu-id="aa5e6-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5e6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa5e6-108">Remarks</span></span>

<span data-ttu-id="aa5e6-109">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="aa5e6-110">Если значение равно **true**, файл содержит по крайней мере один звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-110">If the value is **TRUE**, the file has at least one audio stream.</span></span> <span data-ttu-id="aa5e6-111">В противном случае файл не содержит звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-111">Otherwise, the file does not contain any audio streams.</span></span>

<span data-ttu-id="aa5e6-112">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5e6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="aa5e6-113">Requirements</span></span>



| <span data-ttu-id="aa5e6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="aa5e6-114">Requirement</span></span> | <span data-ttu-id="aa5e6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5e6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5e6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa5e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5e6-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa5e6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa5e6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa5e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5e6-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa5e6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aa5e6-120">Header</span><span class="sxs-lookup"><span data-stu-id="aa5e6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa5e6-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa5e6-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5e6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa5e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5e6-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa5e6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa5e6-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="aa5e6-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="aa5e6-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="aa5e6-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="aa5e6-126">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="aa5e6-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="aa5e6-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="aa5e6-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa5e6-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="aa5e6-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




