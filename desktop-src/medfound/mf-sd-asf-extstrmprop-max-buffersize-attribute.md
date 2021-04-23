---
description: Указывает максимальный размер буфера в байтах, необходимый для потока в файле ASF.
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: Атрибут MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce31dfacd1d53cadcc38b37e1cb755c330a7882f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693612"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a><span data-ttu-id="eadeb-103">MF \_ SD \_ ASF \_ екстстрмпроп \_ Max, \_ атрибут BUFFERSIZE</span><span class="sxs-lookup"><span data-stu-id="eadeb-103">MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="eadeb-104">Указывает максимальный размер буфера в байтах, необходимый для потока в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="eadeb-104">Specifies the maximum buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="eadeb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="eadeb-105">Data type</span></span>

<span data-ttu-id="eadeb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="eadeb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="eadeb-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eadeb-107">Remarks</span></span>

<span data-ttu-id="eadeb-108">Этот атрибут применяется к дескрипторам потоков для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="eadeb-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="eadeb-109">Он соответствует полю "Размер альтернативного буфера" в объекте свойств расширенного потока.</span><span class="sxs-lookup"><span data-stu-id="eadeb-109">It corresponds to the Alternate Buffer Size field in the Extended Stream Properties object.</span></span> <span data-ttu-id="eadeb-110">Дополнительные сведения см. в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="eadeb-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="eadeb-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.</span><span class="sxs-lookup"><span data-stu-id="eadeb-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="eadeb-112">Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="eadeb-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="eadeb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="eadeb-113">Requirements</span></span>



| <span data-ttu-id="eadeb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="eadeb-114">Requirement</span></span> | <span data-ttu-id="eadeb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="eadeb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eadeb-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eadeb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eadeb-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eadeb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eadeb-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eadeb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eadeb-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eadeb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eadeb-120">Header</span><span class="sxs-lookup"><span data-stu-id="eadeb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eadeb-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="eadeb-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadeb-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eadeb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadeb-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eadeb-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eadeb-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="eadeb-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="eadeb-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="eadeb-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="eadeb-126">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="eadeb-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="eadeb-127">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="eadeb-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="eadeb-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="eadeb-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




