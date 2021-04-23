---
description: Приемник ASF-файлов — это реализация Имфмедиасинк, предоставляемая Media Foundation, которую приложение может использовать для архивации данных ASF Media в файл. Сведения об объектной модели приемников ASF Media и общем использовании см. в статье приемники мультимедиа ASF.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Добавление метаданных в приемник файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072793"
---
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="3e239-104">Добавление метаданных в приемник файлов</span><span class="sxs-lookup"><span data-stu-id="3e239-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="3e239-105">Приемник ASF-файлов — это реализация [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , предоставляемая Media Foundation, которую приложение может использовать для архивации данных ASF Media в файл.</span><span class="sxs-lookup"><span data-stu-id="3e239-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="3e239-106">Сведения об объектной модели приемников ASF Media и общем использовании см. в статье [приемники мультимедиа ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="3e239-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="3e239-107">После [создания приемника файлов ASF](creating-the-asf-file-sink.md)его необходимо настроить с помощью сведений о потоках и кодировке в выходном файле.</span><span class="sxs-lookup"><span data-stu-id="3e239-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="3e239-108">Эти процедуры описаны в разделе [Добавление сведений о потоке в приемник файлов ASF](adding-stream-information-to-the-asf-file-sink.md) и [Задание свойств в приемнике файла](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="3e239-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="3e239-109">Кроме того, можно добавить сведения о метаданных, включая пары «имя-значение», такие как «Author», «Title».</span><span class="sxs-lookup"><span data-stu-id="3e239-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="3e239-110">В этом разделе описывается процесс добавления метаданных к приемнику файла, чтобы он появился в окончательном [объекте заголовка ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="3e239-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="3e239-111">Перед созданием топологии кодирования можно добавить сведения о метаданных в приемник файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="3e239-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="3e239-112">Объект ASF Контентинфо для приемника файлов отслеживает свойства метаданных и предоставляется приложению через интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="3e239-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="3e239-113">Некоторые из этих свойств, например "Исвбр", которые указывают, содержит ли файл потоки с переменной скоростью (VBR), устанавливаются автоматически приемником файла путем анализа заданных свойств кодировки потока.</span><span class="sxs-lookup"><span data-stu-id="3e239-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="3e239-114">Полный список свойств см. в разделе «Список атрибутов» документации по формату пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="3e239-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="3e239-115">Использование интерфейса Имфметадата в приемнике файлов ASF</span><span class="sxs-lookup"><span data-stu-id="3e239-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="3e239-116">Запросите объект приемника ASF-файла, чтобы получить указатель на его реализацию интерфейса [**имфметадатапровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="3e239-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="3e239-117">Вызовите [**имфметадатапровидер:: жетмфметадата**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) , чтобы получить указатель [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="3e239-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="3e239-118">Параметр *ппресентатиондескриптор* игнорируется, и приложение может передать **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e239-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="3e239-119">Если приложение передает ноль в качестве идентификатора потока в параметре *двстреамидентифиер* , метод извлекает метаданные, которые применяются ко всему файлу ASF.</span><span class="sxs-lookup"><span data-stu-id="3e239-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="3e239-120">В противном случае извлекается только метаданные для потока.</span><span class="sxs-lookup"><span data-stu-id="3e239-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="3e239-121">Вызовите метод [**имфметадата:: жеталлпропертинамес**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) , чтобы получить список свойств кодирования файла, заданных для мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="3e239-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="3e239-122">Вызовите [**имфметадата:: Property**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) , чтобы получить значения свойств.</span><span class="sxs-lookup"><span data-stu-id="3e239-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="3e239-123">Пример</span><span class="sxs-lookup"><span data-stu-id="3e239-123">Example</span></span>

<span data-ttu-id="3e239-124">В следующем примере кода показано, как перечислить имена и значения свойств, заданные для файла ASF.</span><span class="sxs-lookup"><span data-stu-id="3e239-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3e239-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3e239-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e239-126">Приемники мультимедиа ASF</span><span class="sxs-lookup"><span data-stu-id="3e239-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="3e239-127">Компоненты ASF уровня конвейера</span><span class="sxs-lookup"><span data-stu-id="3e239-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="3e239-128">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e239-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



