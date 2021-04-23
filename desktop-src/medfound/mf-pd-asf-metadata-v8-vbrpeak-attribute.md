---
description: Указывает максимальную скорость потока в файле ASF (с переменной скоростью).
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: Атрибут MF_PD_ASF_METADATA_V8_VBRPEAK (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d987815fea919bb46bbe5758e48d6eb22dad8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546090"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a><span data-ttu-id="cfc51-103">MF \_ PD \_ ASF \_ метаданные \_ V8 \_ вбрпеак Attribute</span><span class="sxs-lookup"><span data-stu-id="cfc51-103">MF\_PD\_ASF\_METADATA\_V8\_VBRPEAK attribute</span></span>

<span data-ttu-id="cfc51-104">Указывает максимальную скорость потока в файле ASF (с переменной скоростью).</span><span class="sxs-lookup"><span data-stu-id="cfc51-104">Specifies the highest momentary bit rate in a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfc51-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cfc51-105">Data type</span></span>

<span data-ttu-id="cfc51-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cfc51-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc51-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfc51-107">Remarks</span></span>

<span data-ttu-id="cfc51-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="cfc51-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="cfc51-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="cfc51-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute.</span></span>

> [!Note]  
> <span data-ttu-id="cfc51-110">Этот атрибут применяется только к файлам, созданным в версии 8 пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="cfc51-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="cfc51-111">Он соответствует атрибуту **вбрпеак** в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cfc51-111">It corresponds to the **VBRPeak** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfc51-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cfc51-112">Requirements</span></span>



| <span data-ttu-id="cfc51-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cfc51-113">Requirement</span></span> | <span data-ttu-id="cfc51-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc51-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc51-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfc51-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc51-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfc51-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cfc51-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfc51-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc51-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cfc51-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cfc51-119">Header</span><span class="sxs-lookup"><span data-stu-id="cfc51-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc51-120"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc51-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc51-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfc51-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc51-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfc51-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cfc51-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="cfc51-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cfc51-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="cfc51-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="cfc51-125">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="cfc51-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="cfc51-126">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="cfc51-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="cfc51-127">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="cfc51-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="cfc51-128">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="cfc51-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




