---
description: Указывает среднюю скорость потока (в битах в секунду) в файле расширенного формата системы (ASF). Этот атрибут соответствует объекту свойств скорость потока, определенному в спецификации ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: Атрибут MF_SD_ASF_STREAMBITRATES_BITRATE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712055"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="07f5f-104">Атрибут скорости MF \_ SD \_ ASF \_ стреамбитратес \_</span><span class="sxs-lookup"><span data-stu-id="07f5f-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="07f5f-105">Указывает среднюю скорость потока (в битах в секунду) в файле расширенного формата системы (ASF).</span><span class="sxs-lookup"><span data-stu-id="07f5f-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="07f5f-106">Этот атрибут соответствует объекту свойств скорость потока, определенному в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="07f5f-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="07f5f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="07f5f-107">Data type</span></span>

<span data-ttu-id="07f5f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="07f5f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="07f5f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07f5f-109">Remarks</span></span>

<span data-ttu-id="07f5f-110">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут и задает его в дескрипторе потока.</span><span class="sxs-lookup"><span data-stu-id="07f5f-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="07f5f-111">Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="07f5f-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="07f5f-112">Значение атрибута равно значению поля среднего бита скорости в объекте свойств частоты разрядов потока.</span><span class="sxs-lookup"><span data-stu-id="07f5f-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f5f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="07f5f-113">Requirements</span></span>



| <span data-ttu-id="07f5f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="07f5f-114">Requirement</span></span> | <span data-ttu-id="07f5f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="07f5f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07f5f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07f5f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07f5f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07f5f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="07f5f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07f5f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07f5f-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07f5f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="07f5f-120">Header</span><span class="sxs-lookup"><span data-stu-id="07f5f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07f5f-121"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="07f5f-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f5f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07f5f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f5f-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07f5f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="07f5f-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="07f5f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="07f5f-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="07f5f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="07f5f-126">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="07f5f-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="07f5f-127">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="07f5f-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="07f5f-128">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="07f5f-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




