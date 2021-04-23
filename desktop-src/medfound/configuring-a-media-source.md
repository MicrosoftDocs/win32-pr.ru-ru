---
description: Настройка источника мультимедиа
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Настройка источника мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105647761"
---
# <a name="configuring-a-media-source"></a><span data-ttu-id="88ebd-103">Настройка источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="88ebd-103">Configuring a Media Source</span></span>

<span data-ttu-id="88ebd-104">При использовании [сопоставителя источников](source-resolver.md) для создания источника мультимедиа можно указать хранилище свойств, которое содержит свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="88ebd-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="88ebd-105">Эти свойства будут использоваться для инициализации источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88ebd-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="88ebd-106">Набор поддерживаемых свойств зависит от реализации источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88ebd-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="88ebd-107">Не каждый источник мультимедиа определяет свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="88ebd-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="88ebd-108">В следующей таблице перечислены свойства конфигурации для источников мультимедиа, предоставляемых в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="88ebd-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="88ebd-109">Сторонние источники мультимедиа могут определять собственные пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="88ebd-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88ebd-110">Источник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="88ebd-110">Media source</span></span></th>
<th><span data-ttu-id="88ebd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="88ebd-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88ebd-112">Источник сети</span><span class="sxs-lookup"><span data-stu-id="88ebd-112">Network source</span></span></td>
<td><span data-ttu-id="88ebd-113">См. раздел <a href="network-source-features.md">функции сетевого источника</a>.</span><span class="sxs-lookup"><span data-stu-id="88ebd-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88ebd-114">Источник носителя ASF</span><span class="sxs-lookup"><span data-stu-id="88ebd-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="88ebd-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="88ebd-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="88ebd-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="88ebd-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="88ebd-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="88ebd-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="88ebd-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="88ebd-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="88ebd-119">Чтобы настроить источник, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="88ebd-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="88ebd-120">Вызовите **пскреатемеморипропертисторе** , чтобы создать новое хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="88ebd-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="88ebd-121">Эта функция возвращает указатель **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="88ebd-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="88ebd-122">Вызовите метод **ипропертисторе:: SetValue** , чтобы задать одно или несколько свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="88ebd-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="88ebd-123">Вызовите одну из функций создания сопоставителя исходного кода, например [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), и передайте указатель **Ипропертисторе** в параметр *ппропс* .</span><span class="sxs-lookup"><span data-stu-id="88ebd-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="88ebd-124">Сопоставитель источников передает указатель **ипропертисторе** непосредственно обработчику схемы или обработчику байтового потока, который создает источник.</span><span class="sxs-lookup"><span data-stu-id="88ebd-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="88ebd-125">Сопоставитель источника не пытается проверить свойства.</span><span class="sxs-lookup"><span data-stu-id="88ebd-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="88ebd-126">Как правило, эти свойства используются для дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="88ebd-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="88ebd-127">Если не указать хранилище свойств, источник мультимедиа по-прежнему должен работать правильно с параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="88ebd-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88ebd-128">См. также</span><span class="sxs-lookup"><span data-stu-id="88ebd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ebd-129">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="88ebd-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



