---
description: В Windows Vista Microsoft Media Foundation предоставляет метаданные через интерфейс Имфметадата.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Поставщики метаданных в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673344"
---
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="2954b-103">Поставщики метаданных в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2954b-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="2954b-104">В Windows Vista Microsoft Media Foundation предоставляет метаданные через интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="2954b-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="2954b-105">Чтение метаданных</span><span class="sxs-lookup"><span data-stu-id="2954b-105">Reading Metadata</span></span>

<span data-ttu-id="2954b-106">Чтобы прочитать метаданные из источника мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2954b-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="2954b-107">Получение указателя на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2954b-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="2954b-108">Для получения указателя **имфмедиасаурце** можно использовать интерфейс [**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="2954b-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="2954b-109">Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , чтобы получить дескриптор представления источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2954b-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="2954b-110">Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) в источнике мультимедиа, чтобы получить указатель на интерфейс [**имфметадатапровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="2954b-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="2954b-111">В параметре *гуидсервице* объекта **мфжетсервице** укажите значение **\_ \_ \_ служба поставщика метаданных MF**.</span><span class="sxs-lookup"><span data-stu-id="2954b-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="2954b-112">Если источник не поддерживает интерфейс **имфметадатапровидер** , **мфжетсервице** возвращает **MF \_ \_ неподдерживаемую \_ службу**.</span><span class="sxs-lookup"><span data-stu-id="2954b-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="2954b-113">Вызовите [**имфметадатапровидер:: жетмфметадата**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) и передайте указатель на дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="2954b-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="2954b-114">Этот метод возвращает указатель на интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="2954b-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="2954b-115">Чтобы получить метаданные уровня потока, сначала вызовите [**имфстреамдескриптор:: жетстреамидентифиер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) , чтобы получить идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="2954b-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="2954b-116">Затем передайте идентификатор потока в параметре *двстреамидентифиер* объекта [**жетмфметадата**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span><span class="sxs-lookup"><span data-stu-id="2954b-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="2954b-117">Чтобы получить метаданные уровня представления, задайте для *двстреамидентифиер* значение 0.</span><span class="sxs-lookup"><span data-stu-id="2954b-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="2954b-118">\[Необязательный \] вызов [**имфметадата:: жеталллангуажес**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) для получения списка языков, на которых доступны метаданные.</span><span class="sxs-lookup"><span data-stu-id="2954b-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="2954b-119">Языки определяются с помощью тегов языка, соответствующих стандарту RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="2954b-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="2954b-120">\[Необязательный \] вызов [**имфметадата:: сетлангуаже**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) для выбора языка.</span><span class="sxs-lookup"><span data-stu-id="2954b-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="2954b-121">\[Необязательный \] вызов [**имфметадата:: жеталлпропертинамес**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) для получения списка имен всех свойств метаданных для этого потока или презентации.</span><span class="sxs-lookup"><span data-stu-id="2954b-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="2954b-122">Вызовите [**имфметадата::-Property**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) , чтобы получить определенное значение свойства метаданных, передав имя свойства.</span><span class="sxs-lookup"><span data-stu-id="2954b-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="2954b-123">В следующем коде показаны шаги 2 – 4.</span><span class="sxs-lookup"><span data-stu-id="2954b-123">The following code shows steps 2–4:</span></span>


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



<span data-ttu-id="2954b-124">В следующем коде показаны шаги 7 – 8.</span><span class="sxs-lookup"><span data-stu-id="2954b-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="2954b-125">Предположим, что `DisplayProperty` является функцией, которая отображает значение **пропвариант** .</span><span class="sxs-lookup"><span data-stu-id="2954b-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2954b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2954b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2954b-127">Метаданные мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2954b-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="2954b-128">Поставщики метаданных оболочки</span><span class="sxs-lookup"><span data-stu-id="2954b-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



