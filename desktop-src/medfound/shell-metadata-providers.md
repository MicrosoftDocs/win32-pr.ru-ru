---
description: Начиная с Windows 7 Microsoft Media Foundation предоставляет метаданные через интерфейс Ипропертисторе.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Поставщики метаданных оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711394"
---
# <a name="shell-metadata-providers"></a><span data-ttu-id="7632d-103">Поставщики метаданных оболочки</span><span class="sxs-lookup"><span data-stu-id="7632d-103">Shell Metadata Providers</span></span>

<span data-ttu-id="7632d-104">Начиная с Windows 7 Microsoft Media Foundation предоставляет метаданные через интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="7632d-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="7632d-105">Метаданные, полученные с помощью процесса, определенного в этом разделе, следует использовать только для доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7632d-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="7632d-106">Запись данных с помощью этого процесса не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7632d-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="7632d-107">Вы можете создать объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) для написания целей с помощью идентификатора класса (CLSID), полученного из [**пслукуппропертихандлерклсид**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span><span class="sxs-lookup"><span data-stu-id="7632d-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="7632d-108">Чтение метаданных</span><span class="sxs-lookup"><span data-stu-id="7632d-108">Reading Metadata</span></span>

<span data-ttu-id="7632d-109">Чтобы прочитать метаданные из источника мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7632d-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="7632d-110">Получение указателя на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7632d-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="7632d-111">Для получения указателя **имфмедиасаурце** можно использовать интерфейс [**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="7632d-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="7632d-112">Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) в источнике мультимедиа, чтобы получить указатель на интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="7632d-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="7632d-113">В параметре *гуидсервице* объекта **мфжетсервице** укажите значение **\_ \_ \_ службы обработчика свойства MF**.</span><span class="sxs-lookup"><span data-stu-id="7632d-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="7632d-114">Если источник не поддерживает интерфейс **ипропертисторе** , **мфжетсервице** возвращает **MF \_ \_ неподдерживаемую \_ службу**.</span><span class="sxs-lookup"><span data-stu-id="7632d-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="7632d-115">Вызовите методы [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы перечислить свойства метаданных.</span><span class="sxs-lookup"><span data-stu-id="7632d-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="7632d-116">Эти действия показаны в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="7632d-116">The following code shows these steps.</span></span> <span data-ttu-id="7632d-117">Предположим, что `DisplayProperty` является функцией, которая отображает значение **пропвариант** .</span><span class="sxs-lookup"><span data-stu-id="7632d-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



<span data-ttu-id="7632d-118">Список ключей свойств метаданных см. в разделе [Свойства метаданных для файлов мультимедиа](metadata-properties-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="7632d-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7632d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7632d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7632d-120">Метаданные мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7632d-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
