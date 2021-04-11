---
description: Создание экземпляра MFT для кодировщика
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Создание экземпляра MFT для кодировщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265511"
---
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="abcb8-103">Создание экземпляра MFT для кодировщика</span><span class="sxs-lookup"><span data-stu-id="abcb8-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="abcb8-104">В Microsoft Media Foundation кодировщики реализуются как [Media Foundation преобразования](media-foundation-transforms.md) (МФТС).</span><span class="sxs-lookup"><span data-stu-id="abcb8-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="abcb8-105">Перед созданием кодировщика сначала необходимо найти кодировщик, который наиболее подходит для ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="abcb8-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="abcb8-106">Аудиокодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="abcb8-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="abcb8-107">Категория: **\_ \_ звуковая \_ кодировщик категории MFT**</span><span class="sxs-lookup"><span data-stu-id="abcb8-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="abcb8-108">Основной тип: Мфмедиатипе \_ Audio</span><span class="sxs-lookup"><span data-stu-id="abcb8-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="abcb8-109">Подтип: Мфаудиоформат \_ WMAudioV9, мфаудиоформат \_ WMAudioV8, мфаудиоформат \_ вмаудио \_ без потерь, мфаудиоформат \_ вмаспдиф</span><span class="sxs-lookup"><span data-stu-id="abcb8-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="abcb8-110">Видеокодеки видео Windows Media</span><span class="sxs-lookup"><span data-stu-id="abcb8-110">Windows Media video codecs</span></span>

    <span data-ttu-id="abcb8-111">Категория: **\_ \_ \_ видеокодировщик категории MFT**</span><span class="sxs-lookup"><span data-stu-id="abcb8-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="abcb8-112">Основной тип: \_ видео мфмедиатипе</span><span class="sxs-lookup"><span data-stu-id="abcb8-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="abcb8-113">Подтип: Мфвидеоформат \_ WVC1, мфвидеоформат \_ WMV3, мфвидеоформат \_ WMV2, мфвидеоформат \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="abcb8-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="abcb8-114">Media Foundation предоставляет несколько функций, которые могут вызываться приложением для перечисления различных кодировщиков, доступных в системе.</span><span class="sxs-lookup"><span data-stu-id="abcb8-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="abcb8-115">Кодировщики регистрируются в виде COM-объектов, а запись реестра соответствует стандартному формату фабрик классов COM.</span><span class="sxs-lookup"><span data-stu-id="abcb8-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="abcb8-116">Реестр поддерживает идентификаторы CLSID для кодировщиков, которые классифицируются по формату мультимедиа (аудио или видео).</span><span class="sxs-lookup"><span data-stu-id="abcb8-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="abcb8-117">Идентификаторы классов кодировщиков Windows Media определяются как константы в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="abcb8-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="abcb8-118">В Media Foundation кодировщики можно зарегистрировать с помощью вызовов [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) или [**мфтрегистерлокалбиклсид**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) , указав категории, Поддерживаемые входные типы и поддерживаемые типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="abcb8-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="abcb8-119">После успешной регистрации с помощью этих функций МФТС рассматриваются функциями перечисления Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="abcb8-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="abcb8-120">Для создания экземпляра файла MFT кодировщика приложение имеет следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="abcb8-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="abcb8-121">Создайте объект MFT кодировщика напрямую и получите указатель на интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="abcb8-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="abcb8-122">Дополнительные сведения см. в разделе [Создание кодировщика с помощью CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span><span class="sxs-lookup"><span data-stu-id="abcb8-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="abcb8-123">Создайте экземпляр объекта активации для файла MFT кодировщика и получите указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="abcb8-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="abcb8-124">Дополнительные сведения см. [в разделе Использование объектов активации кодировщика](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="abcb8-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="abcb8-125">Если приложение использует [компоненты ASF уровня конвейера](pipeline-layer-asf-components.md) для кодирования файла в формат ASF, необходимо вставить файл MFT кодировщика в конвейер в качестве узла преобразования.</span><span class="sxs-lookup"><span data-stu-id="abcb8-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="abcb8-126">При создании узла преобразования в топологии кодирования можно либо задать тип объекта в качестве указателя на интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , либо объект [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="abcb8-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="abcb8-127">Media Foundation предоставляет объекты активации для кодировщиков Windows Media, чтобы их можно было легко задать в качестве узла преобразования в топологии кодирования.</span><span class="sxs-lookup"><span data-stu-id="abcb8-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="abcb8-128">При разрешении топологии сеанс мультимедиа использует объект активации для создания экземпляра файла MFT кодировщика.</span><span class="sxs-lookup"><span data-stu-id="abcb8-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abcb8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="abcb8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abcb8-130">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="abcb8-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



