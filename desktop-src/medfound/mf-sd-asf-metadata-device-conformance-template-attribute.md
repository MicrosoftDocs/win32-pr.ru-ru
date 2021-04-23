---
description: Указывает шаблон соответствия устройств для потока в файле ASF (Расширенный системный формат).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: Атрибут MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712056"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="a2598-103">\_ \_ \_ \_ \_ Атрибут шаблона соответствия для устройства метаданных \_ MF SD ASF</span><span class="sxs-lookup"><span data-stu-id="a2598-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="a2598-104">Указывает шаблон соответствия устройств для потока в файле ASF (Расширенный системный формат).</span><span class="sxs-lookup"><span data-stu-id="a2598-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2598-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a2598-105">Data type</span></span>

<span data-ttu-id="a2598-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="a2598-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="a2598-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2598-107">Remarks</span></span>

<span data-ttu-id="a2598-108">Этот атрибут применяется к дескрипторам потоков для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="a2598-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="a2598-109">Дополнительные сведения о шаблонах соответствия устройств см. в разделе "Параметры шаблона согласованности устройств" раздела Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a2598-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="a2598-110">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="a2598-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2598-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a2598-111">Requirements</span></span>



| <span data-ttu-id="a2598-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a2598-112">Requirement</span></span> | <span data-ttu-id="a2598-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a2598-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2598-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2598-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a2598-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2598-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2598-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2598-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a2598-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2598-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a2598-118">Header</span><span class="sxs-lookup"><span data-stu-id="a2598-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2598-119"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2598-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2598-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2598-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2598-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2598-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2598-122">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="a2598-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="a2598-123">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="a2598-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="a2598-124">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="a2598-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="a2598-125">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="a2598-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2598-126">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="a2598-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




