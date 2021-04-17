---
description: Указывает средний размер буфера, необходимый для файла ASF с переменной скоростью (VBR).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: Атрибут MF_PD_ASF_METADATA_V8_BUFFERAVERAGE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711301"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="273e5-103">MF \_ PD \_ ASF \_ метаданные \_ V8 \_ буфферавераже Attribute</span><span class="sxs-lookup"><span data-stu-id="273e5-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="273e5-104">Указывает средний размер буфера, необходимый для файла ASF с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="273e5-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="273e5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="273e5-105">Data type</span></span>

<span data-ttu-id="273e5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="273e5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="273e5-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="273e5-107">Remarks</span></span>

<span data-ttu-id="273e5-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="273e5-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="273e5-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут, который применяется к дескриптору представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="273e5-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="273e5-110">Этот атрибут применяется только к файлам, созданным в версии 8 пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="273e5-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="273e5-111">Он соответствует атрибуту **буфферавераже** в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="273e5-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="273e5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="273e5-112">Requirements</span></span>



| <span data-ttu-id="273e5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="273e5-113">Requirement</span></span> | <span data-ttu-id="273e5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="273e5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="273e5-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="273e5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="273e5-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="273e5-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="273e5-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="273e5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="273e5-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="273e5-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="273e5-119">Header</span><span class="sxs-lookup"><span data-stu-id="273e5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="273e5-120"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="273e5-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="273e5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="273e5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273e5-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="273e5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="273e5-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="273e5-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="273e5-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="273e5-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="273e5-125">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="273e5-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="273e5-126">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="273e5-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="273e5-127">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="273e5-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="273e5-128">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="273e5-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




