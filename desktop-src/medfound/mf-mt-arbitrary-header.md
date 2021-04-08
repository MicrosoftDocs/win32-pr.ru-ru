---
description: Данные конкретного типа для двоичного потока в файле ASF.
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Атрибут MF_MT_ARBITRARY_HEADER (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080483"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="269bc-103">\_ \_ Необязательный \_ атрибут заголовка MF MT</span><span class="sxs-lookup"><span data-stu-id="269bc-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="269bc-104">Данные конкретного типа для двоичного потока в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="269bc-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="269bc-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="269bc-105">Data type</span></span>

<span data-ttu-id="269bc-106">**[**MT \_ ПРОИЗВОЛЬНЫй \_ заголовок**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** хранится в виде **\[ \] байта**</span><span class="sxs-lookup"><span data-stu-id="269bc-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="269bc-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="269bc-107">Get/set</span></span>

<span data-ttu-id="269bc-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="269bc-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="269bc-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="269bc-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="269bc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="269bc-110">Remarks</span></span>

<span data-ttu-id="269bc-111">Файлы ASF могут содержать потоки с двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="269bc-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="269bc-112">Атрибут MF \_ \_ Header с произвольным \_ заголовком в типе мультимедиа [**содержит \_ произвольную структуру \_ заголовков MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) , описывающую поток.</span><span class="sxs-lookup"><span data-stu-id="269bc-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="269bc-113">В дополнение к \_ \_ атрибуту заголовка MF MT произвольный \_ заголовок Тип мультимедиа для двоичного потока ASF содержит следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="269bc-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="269bc-114">attribute</span><span class="sxs-lookup"><span data-stu-id="269bc-114">Attribute</span></span>                                                 | <span data-ttu-id="269bc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="269bc-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="269bc-116">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="269bc-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="269bc-117">Значение атрибута — **мфмедиатипе \_ binary**.</span><span class="sxs-lookup"><span data-stu-id="269bc-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="269bc-118">\_ \_ необязательный \_ формат MF MT</span><span class="sxs-lookup"><span data-stu-id="269bc-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="269bc-119">Содержит дополнительные данные формата.</span><span class="sxs-lookup"><span data-stu-id="269bc-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="269bc-120">В пакете SDK для формата Windows Media двоичные потоки называются *произвольными потоками* или *произвольными потоками данных*.</span><span class="sxs-lookup"><span data-stu-id="269bc-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="269bc-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="269bc-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="269bc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="269bc-122">Requirements</span></span>



| <span data-ttu-id="269bc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="269bc-123">Requirement</span></span> | <span data-ttu-id="269bc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="269bc-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="269bc-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="269bc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="269bc-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="269bc-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="269bc-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="269bc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="269bc-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="269bc-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="269bc-129">Header</span><span class="sxs-lookup"><span data-stu-id="269bc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="269bc-130"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="269bc-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="269bc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="269bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269bc-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="269bc-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="269bc-133">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="269bc-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




