---
description: Настройка кодека МФТС
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Настройка кодека МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496827"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="df3e8-103">Настройка кодека МФТС</span><span class="sxs-lookup"><span data-stu-id="df3e8-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="df3e8-104">В этом разделе описывается процесс настройки кодека МФТС.</span><span class="sxs-lookup"><span data-stu-id="df3e8-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="df3e8-105">Каждый кодек имеет определенные процедуры, но сведения, общие для всех, описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="df3e8-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="df3e8-106">Настройка входных и выходных файлов MFT</span><span class="sxs-lookup"><span data-stu-id="df3e8-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="df3e8-107">Каждый файл MFT поддерживает определенные типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="df3e8-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="df3e8-108">Поддерживаемые входные типы можно получить, повторно вызвав [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), увеличивая индекс типа с каждым вызовом.</span><span class="sxs-lookup"><span data-stu-id="df3e8-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="df3e8-109">При обнаружении соответствующего типа задайте тип входных данных, вызвав [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="df3e8-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="df3e8-110">Затем можно повторить процесс для типа выходных данных с помощью вызовов [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) и [**Имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="df3e8-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="df3e8-111">Необходимо запрашивать или задавать доступные выходные типы только после установки входного типа.</span><span class="sxs-lookup"><span data-stu-id="df3e8-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="df3e8-112">Настройка кодека МФТС для кодирования</span><span class="sxs-lookup"><span data-stu-id="df3e8-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="df3e8-113">Все видеокодеки Windows Media Audio и Video поддерживают различные функции кодирования.</span><span class="sxs-lookup"><span data-stu-id="df3e8-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="df3e8-114">Эти функции обычно настраиваются путем установки свойств в MFT с помощью методов интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="df3e8-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="df3e8-115">Некоторые свойства настраиваются с помощью специализированных интерфейсов кодека.</span><span class="sxs-lookup"><span data-stu-id="df3e8-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="df3e8-116">Эти интерфейсы перечислены для каждого кодека в разделе [объекты кодека](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="df3e8-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="df3e8-117">Ниже приведен общий порядок операций для настройки кодировки MFT.</span><span class="sxs-lookup"><span data-stu-id="df3e8-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="df3e8-118">Настройте необходимые функции кодека с помощью методов **ипропертисторе**.</span><span class="sxs-lookup"><span data-stu-id="df3e8-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="df3e8-119">При необходимости используйте интерфейсы кодека MFT для настройки дополнительных функций.</span><span class="sxs-lookup"><span data-stu-id="df3e8-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="df3e8-120">Настройте типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="df3e8-120">Configure the input and output types.</span></span> <span data-ttu-id="df3e8-121">Порядок, в котором должны настраиваться типы, зависит от отдельных кодеков.</span><span class="sxs-lookup"><span data-stu-id="df3e8-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="df3e8-122">Дополнительные сведения см. в разделе [Работа с аудио](workingwithaudio.md) и [Работа с видео](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="df3e8-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="df3e8-123">Настройка кодека МФТС для декодирования</span><span class="sxs-lookup"><span data-stu-id="df3e8-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="df3e8-124">Декодирование проще, чем кодирование, так как поддерживается меньше возможностей декодера.</span><span class="sxs-lookup"><span data-stu-id="df3e8-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="df3e8-125">Ниже приведен общий порядок операций для настройки декодирования MFT.</span><span class="sxs-lookup"><span data-stu-id="df3e8-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="df3e8-126">Настройте необходимые функции декодера с помощью методов **ипропертисторе**.</span><span class="sxs-lookup"><span data-stu-id="df3e8-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="df3e8-127">Установите тип входных данных в тип, используемый для выходных данных кодировщика.</span><span class="sxs-lookup"><span data-stu-id="df3e8-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="df3e8-128">Настройте тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="df3e8-128">Configure the output type.</span></span> <span data-ttu-id="df3e8-129">Поддерживаемые типы вывода различаются для различных входных данных.</span><span class="sxs-lookup"><span data-stu-id="df3e8-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="df3e8-130">Важно использовать тот же тип носителя для ввода декодера, что использовалось для выходных данных кодировщика.</span><span class="sxs-lookup"><span data-stu-id="df3e8-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="df3e8-131">Это обусловлено тем, что видеокодеки Windows Media Audio и Video используют форматы мультимедиа с дополнительными данными.</span><span class="sxs-lookup"><span data-stu-id="df3e8-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="df3e8-132">Без данных расширенного формата декодировать сжатое содержимое нельзя.</span><span class="sxs-lookup"><span data-stu-id="df3e8-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="df3e8-133">См. также</span><span class="sxs-lookup"><span data-stu-id="df3e8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df3e8-134">Работа с кодеками МФТС</span><span class="sxs-lookup"><span data-stu-id="df3e8-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



