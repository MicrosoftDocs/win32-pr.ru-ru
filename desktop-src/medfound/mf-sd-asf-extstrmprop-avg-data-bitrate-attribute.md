---
description: Указывает среднюю скорость передачи данных (в битах в секунду) для потока в файле расширенных систем формата (ASF).
ms.assetid: 3a0b39ab-e9a9-49df-a321-a88559aec16f
title: Атрибут MF_SD_ASF_EXTSTRMPROP_AVG_DATA_BITRATE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18789fbd18f063c59de712cf1b1b6bdac1c38a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647493"
---
# <a name="mf_sd_asf_extstrmprop_avg_data_bitrate-attribute"></a><span data-ttu-id="f2644-103">\_Атрибут скорости \_ \_ екстстрмпроп \_ средний размер \_ данных \_ для MF SD ASF</span><span class="sxs-lookup"><span data-stu-id="f2644-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE attribute</span></span>

<span data-ttu-id="f2644-104">Указывает среднюю скорость передачи данных (в битах в секунду) для потока в файле расширенных систем формата (ASF).</span><span class="sxs-lookup"><span data-stu-id="f2644-104">Specifies the average data bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2644-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f2644-105">Data type</span></span>

<span data-ttu-id="f2644-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f2644-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f2644-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2644-107">Remarks</span></span>

<span data-ttu-id="f2644-108">Этот атрибут применяется к дескрипторам потоков для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="f2644-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="f2644-109">Он соответствует полю «скорость передачи данных» в объекте «свойства» расширенного потока и определяет частоту утечки, используемую в модели «сегмент утечки».</span><span class="sxs-lookup"><span data-stu-id="f2644-109">It corresponds to the Data Bit Rate field in the Extended Stream Properties object, and defines the leak rate used in the "leaky bucket" model.</span></span> <span data-ttu-id="f2644-110">Дополнительные сведения см. в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="f2644-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="f2644-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="f2644-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="f2644-112">Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="f2644-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2644-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f2644-113">Requirements</span></span>



| <span data-ttu-id="f2644-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f2644-114">Requirement</span></span> | <span data-ttu-id="f2644-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f2644-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2644-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2644-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2644-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2644-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f2644-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2644-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2644-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2644-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2644-120">Header</span><span class="sxs-lookup"><span data-stu-id="f2644-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2644-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2644-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2644-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2644-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2644-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2644-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2644-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f2644-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f2644-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f2644-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f2644-126">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="f2644-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="f2644-127">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="f2644-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2644-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="f2644-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




