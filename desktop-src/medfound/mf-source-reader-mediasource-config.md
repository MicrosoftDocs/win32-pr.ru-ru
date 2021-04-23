---
description: Содержит свойства конфигурации для модуля чтения исходного кода.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: Атрибут MF_SOURCE_READER_MEDIASOURCE_CONFIG (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703475"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="127f7-103">\_ \_ \_ Атрибут конфигурации медиасаурце для чтения источника MF \_</span><span class="sxs-lookup"><span data-stu-id="127f7-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="127f7-104">Содержит свойства конфигурации для [модуля чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="127f7-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="127f7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="127f7-105">Data type</span></span>

<span data-ttu-id="127f7-106">**Ипропертисторе \* *_ хранится как _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="127f7-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="127f7-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="127f7-107">Get/set</span></span>

<span data-ttu-id="127f7-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="127f7-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="127f7-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="127f7-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="127f7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="127f7-110">Remarks</span></span>

<span data-ttu-id="127f7-111">Значение этого атрибута является указателем на интерфейс **ипропертисторе** хранилища свойств.</span><span class="sxs-lookup"><span data-stu-id="127f7-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="127f7-112">Этот атрибут можно использовать для передачи свойств конфигурации источнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="127f7-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="127f7-113">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="127f7-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="127f7-114">**мфкреатесаурцереадерфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="127f7-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="127f7-115">**мфкреатесаурцереадерфромурл**</span><span class="sxs-lookup"><span data-stu-id="127f7-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="127f7-116">Модуль чтения исходного кода передает указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="127f7-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="127f7-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="127f7-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="127f7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="127f7-118">Requirements</span></span>



| <span data-ttu-id="127f7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="127f7-119">Requirement</span></span> | <span data-ttu-id="127f7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="127f7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="127f7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="127f7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="127f7-122">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="127f7-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="127f7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="127f7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="127f7-124">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="127f7-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="127f7-125">Header</span><span class="sxs-lookup"><span data-stu-id="127f7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="127f7-126"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="127f7-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127f7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="127f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127f7-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="127f7-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="127f7-129">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="127f7-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="127f7-130">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="127f7-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




