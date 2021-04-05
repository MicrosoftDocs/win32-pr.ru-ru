---
description: Синхронизированный доступный мультимедийный обмен (SAMI) — это формат для добавления субтитров к цифровым носителям.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Источник носителя SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081706"
---
# <a name="sami-media-source"></a><span data-ttu-id="cbb02-103">Источник носителя SAMI</span><span class="sxs-lookup"><span data-stu-id="cbb02-103">SAMI Media Source</span></span>

<span data-ttu-id="cbb02-104">Синхронизированный доступный мультимедийный обмен (SAMI) — это формат для добавления субтитров к цифровым носителям.</span><span class="sxs-lookup"><span data-stu-id="cbb02-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="cbb02-105">Заголовки хранятся в отдельном текстовом файле с расширением. SMI или. Sami.</span><span class="sxs-lookup"><span data-stu-id="cbb02-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="cbb02-106">В Media Foundation файлы заголовков SAMId поддерживаются через источник носителя SAMI.</span><span class="sxs-lookup"><span data-stu-id="cbb02-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="cbb02-107">Используйте [сопоставитель источников](source-resolver.md) , чтобы создать экземпляр источника носителя Sami из URL-адреса или потока байтов.</span><span class="sxs-lookup"><span data-stu-id="cbb02-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="cbb02-108">Media Foundation не предоставляет компонент, который отображает субтитры SAMId.</span><span class="sxs-lookup"><span data-stu-id="cbb02-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="cbb02-109">Приложение должно интерпретировать данные заголовка, полученные от источника на носителе SAMI.</span><span class="sxs-lookup"><span data-stu-id="cbb02-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="cbb02-110">Ниже приведен пример файла SAMI.</span><span class="sxs-lookup"><span data-stu-id="cbb02-110">The following shows an example SAMI file.</span></span>

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

<span data-ttu-id="cbb02-111">`<STYLE>`Элемент содержит сведения о стиле.</span><span class="sxs-lookup"><span data-stu-id="cbb02-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="cbb02-112">Этот пример содержит базовый стиль для `<P>` элементов, а также два именованных стиля: "Стандартный" и "хилите".</span><span class="sxs-lookup"><span data-stu-id="cbb02-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="cbb02-113">Именованные стили используются для изменения базового стиля.</span><span class="sxs-lookup"><span data-stu-id="cbb02-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="cbb02-114">Заголовки помещаются в `<SYNC>` элементы.</span><span class="sxs-lookup"><span data-stu-id="cbb02-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="cbb02-115">Атрибут start задает время презентации в миллисекундах для этого заголовка.</span><span class="sxs-lookup"><span data-stu-id="cbb02-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="cbb02-116">Заголовки в этом примере приведены на двух языках, указанных в тегах языка RFC-1766, «EN-US» и «fr-FR».</span><span class="sxs-lookup"><span data-stu-id="cbb02-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="cbb02-117">В заголовках языки идентифицируются по именам их классов. в этом случае "ЕНУСКК" и "ФРФРКК".</span><span class="sxs-lookup"><span data-stu-id="cbb02-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="cbb02-118">Источник носителя SAMId создает один поток мультимедиа для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="cbb02-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="cbb02-119">По умолчанию выбирается первый поток, и оставшиеся выбранные потоки отменяются.</span><span class="sxs-lookup"><span data-stu-id="cbb02-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="cbb02-120">Приложение может изменить выбор потока, вызвав [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) и [**Имфпресентатиондескриптор::D еселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="cbb02-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="cbb02-121">Каждый дескриптор потока содержит следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="cbb02-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="cbb02-122">attribute</span><span class="sxs-lookup"><span data-stu-id="cbb02-122">Attribute</span></span>                                                       | <span data-ttu-id="cbb02-123">Описание</span><span class="sxs-lookup"><span data-stu-id="cbb02-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="cbb02-124">**\_язык MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="cbb02-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="cbb02-125">Тег языка, заданный `lang` атрибутом.</span><span class="sxs-lookup"><span data-stu-id="cbb02-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="cbb02-126">**\_язык MF SD \_ Sami \_**</span><span class="sxs-lookup"><span data-stu-id="cbb02-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="cbb02-127">Имя языка, заданное `Name` атрибутом.</span><span class="sxs-lookup"><span data-stu-id="cbb02-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="cbb02-128">Каждый поток имеет следующий тип носителя:</span><span class="sxs-lookup"><span data-stu-id="cbb02-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="cbb02-129">attribute</span><span class="sxs-lookup"><span data-stu-id="cbb02-129">Attribute</span></span>                                                                            | <span data-ttu-id="cbb02-130">Значение</span><span class="sxs-lookup"><span data-stu-id="cbb02-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="cbb02-131">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cbb02-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="cbb02-132">**Мфмедиатипе \_ Sami**</span><span class="sxs-lookup"><span data-stu-id="cbb02-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="cbb02-133">**MF \_ — \_ все \_ \_ независимые примеры**</span><span class="sxs-lookup"><span data-stu-id="cbb02-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="cbb02-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="cbb02-134">**TRUE**</span></span>              |



 

<span data-ttu-id="cbb02-135">Источник SAMI предоставляет каждый заголовок в отдельном образце носителя.</span><span class="sxs-lookup"><span data-stu-id="cbb02-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="cbb02-136">Образец метки времени и длительность являются производными от `<SYNC>` элемента.</span><span class="sxs-lookup"><span data-stu-id="cbb02-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="cbb02-137">Буфер мультимедиа, содержащийся в примере, содержит заголовок в виде текста ASCII.</span><span class="sxs-lookup"><span data-stu-id="cbb02-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="cbb02-138">Стиль заголовка внедряется в заголовок в виде встроенного `STYLE` атрибута.</span><span class="sxs-lookup"><span data-stu-id="cbb02-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="cbb02-139">Например, при наличии предыдущего файла SAMI и использовании в потоке английского языка со стилями по умолчанию первый буфер мультимедиа будет содержать следующие данные.</span><span class="sxs-lookup"><span data-stu-id="cbb02-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="cbb02-140">(Разрывы строк могут отличаться от показанных здесь.)</span><span class="sxs-lookup"><span data-stu-id="cbb02-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="cbb02-141">Стили SAMI</span><span class="sxs-lookup"><span data-stu-id="cbb02-141">SAMI Styles</span></span>

<span data-ttu-id="cbb02-142">Чтобы изменить текущий стиль, используйте интерфейс [**имфсамистиле**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="cbb02-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="cbb02-143">Этот интерфейс получается путем вызова [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в источнике носителя Sami.</span><span class="sxs-lookup"><span data-stu-id="cbb02-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="cbb02-144">(Если вы используете источник мультимедиа SAMI с сеансом мультимедиа, вызовите метод **WebService** в сеансе мультимедиа.) Идентификатор службы — это **\_ \_ Служба MF Sami**.</span><span class="sxs-lookup"><span data-stu-id="cbb02-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="cbb02-145">В следующем примере задается текущий стиль SAMI, заданный параметром index.</span><span class="sxs-lookup"><span data-stu-id="cbb02-145">The following example sets the current SAMI style, specified by index.</span></span>


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



<span data-ttu-id="cbb02-146">Этот пример вызывает следующие методы в источнике носителя SAMI:</span><span class="sxs-lookup"><span data-stu-id="cbb02-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="cbb02-147">[**Имфсамистиле:: жетстилекаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) возвращает число стилей.</span><span class="sxs-lookup"><span data-stu-id="cbb02-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="cbb02-148">[**Имфсамистиле::**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) возвращает список имен стилей, сохраненных в **пропвариант**.</span><span class="sxs-lookup"><span data-stu-id="cbb02-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="cbb02-149">[**Имфсамистиле:: сетселектедстиле**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) задает стиль по имени.</span><span class="sxs-lookup"><span data-stu-id="cbb02-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="cbb02-150">Список имен стилей также хранится в дескрипторе презентации в атрибуте [**MF \_ PD \_ Sami \_ стилелист**](mf-pd-sami-stylelist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb02-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb02-151">См. также</span><span class="sxs-lookup"><span data-stu-id="cbb02-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb02-152">Источники и приемники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cbb02-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="cbb02-153">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cbb02-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



