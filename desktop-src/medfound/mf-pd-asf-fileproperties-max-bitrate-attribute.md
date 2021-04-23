---
description: Указывает максимальную скорость мгновенного прохождения (в битах в секунду) для файла расширенных систем форматирования (ASF).
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: Атрибут MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909592"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="b8675-103">\_Атрибут максимальной скорости MF PD \_ ASF \_ филепропертиес \_ \_</span><span class="sxs-lookup"><span data-stu-id="b8675-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="b8675-104">Указывает максимальную скорость мгновенного прохождения (в битах в секунду) для файла расширенных систем форматирования (ASF).</span><span class="sxs-lookup"><span data-stu-id="b8675-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8675-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b8675-105">Data type</span></span>

<span data-ttu-id="b8675-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b8675-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b8675-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8675-107">Remarks</span></span>

<span data-ttu-id="b8675-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="b8675-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b8675-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="b8675-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8675-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b8675-110">Requirements</span></span>



| <span data-ttu-id="b8675-111">Требование</span><span class="sxs-lookup"><span data-stu-id="b8675-111">Requirement</span></span> | <span data-ttu-id="b8675-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b8675-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8675-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8675-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b8675-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8675-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8675-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8675-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b8675-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8675-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b8675-117">Header</span><span class="sxs-lookup"><span data-stu-id="b8675-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8675-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8675-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8675-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8675-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8675-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8675-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8675-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="b8675-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b8675-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b8675-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b8675-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="b8675-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b8675-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="b8675-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8675-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="b8675-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b8675-126">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="b8675-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




