---
description: Дополнительные данные формата для двоичного потока в файле ASF.
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Атрибут MF_MT_ARBITRARY_FORMAT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712261"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="d0a51-103">\_ \_ Необязательный \_ атрибут формата MF MT</span><span class="sxs-lookup"><span data-stu-id="d0a51-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="d0a51-104">Дополнительные данные формата для двоичного потока в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="d0a51-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0a51-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d0a51-105">Data type</span></span>

<span data-ttu-id="d0a51-106">**ДВУХБАЙТОВЫХ\[\]**</span><span class="sxs-lookup"><span data-stu-id="d0a51-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="d0a51-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="d0a51-107">Get/set</span></span>

<span data-ttu-id="d0a51-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="d0a51-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="d0a51-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="d0a51-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a51-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0a51-110">Remarks</span></span>

<span data-ttu-id="d0a51-111">Приложения могут использовать двоичные потоки для хранения пользовательских типов данных.</span><span class="sxs-lookup"><span data-stu-id="d0a51-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="d0a51-112">Источник мультимедиа ASF считает значение этого атрибута непрозрачным BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="d0a51-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="d0a51-113">Элемент **форматтипе** в структуре [**\_ произвольного \_ заголовка MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) определяет макет данных формата.</span><span class="sxs-lookup"><span data-stu-id="d0a51-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="d0a51-114">Эта структура соответствует полю данных формата данных, характерных для конкретного типа, в объекте свойства потока в файлах, где тип потока является **\_ двоичным \_ носителем ASF**.</span><span class="sxs-lookup"><span data-stu-id="d0a51-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="d0a51-115">Дополнительные сведения см. в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="d0a51-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="d0a51-116">В пакете SDK для формата Windows Media двоичные потоки называются *произвольными потоками* или *произвольными потоками данных*.</span><span class="sxs-lookup"><span data-stu-id="d0a51-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="d0a51-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d0a51-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a51-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d0a51-118">Requirements</span></span>



| <span data-ttu-id="d0a51-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d0a51-119">Requirement</span></span> | <span data-ttu-id="d0a51-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d0a51-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a51-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0a51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a51-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0a51-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d0a51-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0a51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a51-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0a51-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d0a51-125">Header</span><span class="sxs-lookup"><span data-stu-id="d0a51-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a51-126"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a51-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a51-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0a51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a51-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0a51-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0a51-129">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d0a51-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0a51-130">\_ \_ произвольный заголовок MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d0a51-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




