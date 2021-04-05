---
description: Указывает смещение (в байтах) от начала файла расширенного формата системы (ASF) до начала первого пакета данных.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: Атрибут MF_PD_ASF_DATA_START_OFFSET (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912159"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="27314-103">\_ \_ \_ \_ Атрибут смещения начальной загрузки данных MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="27314-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="27314-104">Указывает смещение (в байтах) от начала файла расширенного формата системы (ASF) до начала первого пакета данных.</span><span class="sxs-lookup"><span data-stu-id="27314-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="27314-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="27314-105">Data type</span></span>

<span data-ttu-id="27314-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="27314-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="27314-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27314-107">Remarks</span></span>

<span data-ttu-id="27314-108">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="27314-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="27314-109">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="27314-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="27314-110">Требования</span><span class="sxs-lookup"><span data-stu-id="27314-110">Requirements</span></span>



| <span data-ttu-id="27314-111">Требование</span><span class="sxs-lookup"><span data-stu-id="27314-111">Requirement</span></span> | <span data-ttu-id="27314-112">Значение</span><span class="sxs-lookup"><span data-stu-id="27314-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="27314-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27314-113">Minimum supported client</span></span><br/> | <span data-ttu-id="27314-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27314-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="27314-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27314-115">Minimum supported server</span></span><br/> | <span data-ttu-id="27314-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27314-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="27314-117">Header</span><span class="sxs-lookup"><span data-stu-id="27314-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="27314-118"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="27314-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27314-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27314-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27314-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27314-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="27314-121">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="27314-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="27314-122">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="27314-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="27314-123">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="27314-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="27314-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="27314-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="27314-125">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="27314-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




