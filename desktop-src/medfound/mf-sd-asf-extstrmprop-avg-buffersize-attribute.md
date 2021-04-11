---
description: Указывает средний размер буфера (в байтах), необходимый для потока в файле расширенных систем формата (ASF).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: Атрибут MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c3fc186c2c07ccff1993f1db07d89150a98541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910803"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a><span data-ttu-id="f9680-103">% MF \_ SD \_ ASF екстстрмпроп, \_ \_ \_ атрибут AVG BUFFERSIZE</span><span class="sxs-lookup"><span data-stu-id="f9680-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="f9680-104">Указывает средний размер буфера (в байтах), необходимый для потока в файле расширенных систем формата (ASF).</span><span class="sxs-lookup"><span data-stu-id="f9680-104">Specifies the average buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f9680-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f9680-105">Data type</span></span>

<span data-ttu-id="f9680-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f9680-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f9680-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9680-107">Remarks</span></span>

<span data-ttu-id="f9680-108">Этот атрибут применяется к дескрипторам потоков для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="f9680-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="f9680-109">Он соответствует полю размер буфера в объекте свойств расширенного потока и определяет размер контейнера, используемый в модели "сегмент утечки".</span><span class="sxs-lookup"><span data-stu-id="f9680-109">It corresponds to the Buffer Size field in the Extended Stream Properties object, and defines the bucket size used in the "leaky bucket" model.</span></span> <span data-ttu-id="f9680-110">Дополнительные сведения см. в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="f9680-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="f9680-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="f9680-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="f9680-112">Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="f9680-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9680-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f9680-113">Requirements</span></span>



| <span data-ttu-id="f9680-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f9680-114">Requirement</span></span> | <span data-ttu-id="f9680-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f9680-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9680-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9680-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f9680-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9680-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9680-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9680-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f9680-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9680-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9680-120">Header</span><span class="sxs-lookup"><span data-stu-id="f9680-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9680-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9680-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9680-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9680-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9680-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9680-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9680-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f9680-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f9680-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f9680-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f9680-126">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="f9680-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="f9680-127">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="f9680-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9680-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="f9680-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




