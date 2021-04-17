---
title: Произвольные и предварительно сжатые входные потоки
description: Произвольные и предварительно сжатые входные потоки
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Расширенный системный формат (ASF), произвольные входные потоки
- ASF (Расширенный системный формат), произвольные входные потоки
- профили, произвольные входные потоки
- кодеки, произвольные входные потоки
- Расширенный системный формат (ASF), предварительно сжатые входные потоки
- ASF (Расширенный системный формат), предварительно сжатые входные потоки
- профили, предварительно сжатые входные потоки
- кодеки, предварительно сжатые входные потоки
- предварительно сжатые входные потоки
- произвольные входные потоки
- потоки, произвольные входные потоковые данные
- потоки, предварительно сжатые входные данные потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105700819"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="1091f-115">Произвольные и предварительно сжатые входные потоки</span><span class="sxs-lookup"><span data-stu-id="1091f-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="1091f-116">Только входные данные, которые должны быть сжаты одним из кодеков Windows Media, имеют несколько возможных входов.</span><span class="sxs-lookup"><span data-stu-id="1091f-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="1091f-117">Другими типами возможных входов являются произвольные входные данные и предсжатые входные данные.</span><span class="sxs-lookup"><span data-stu-id="1091f-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="1091f-118">Требования для форматов ввода для этих типов описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1091f-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="1091f-119">Произвольные входные потоки</span><span class="sxs-lookup"><span data-stu-id="1091f-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="1091f-120">Входные данные для произвольных типов потоков совпадают с форматами потока, описанными в профиле.</span><span class="sxs-lookup"><span data-stu-id="1091f-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="1091f-121">Для этих типов не нужно задавать входные форматы.</span><span class="sxs-lookup"><span data-stu-id="1091f-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="1091f-122">Предварительно сжатые входные потоки</span><span class="sxs-lookup"><span data-stu-id="1091f-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="1091f-123">При копировании потока из одного файла в другой передаются уже сжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="1091f-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="1091f-124">В этом случае необходимо задать для объекта входных свойств **значение NULL** , чтобы сообщить средству записи о необходимости проверки передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="1091f-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="1091f-125">Чтобы задать формат входных данных равным **null**, вызовите метод [**Ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) и передайте **значение NULL** в качестве второго параметра.</span><span class="sxs-lookup"><span data-stu-id="1091f-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="1091f-126">При вызове этого метода с параметром **null** необходимо сделать вызов перед вызовом [**бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="1091f-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="1091f-127">При использовании предварительно сжатых потоков необходимо вручную скопировать сведения о кодека в заголовок файла перед записью.</span><span class="sxs-lookup"><span data-stu-id="1091f-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="1091f-128">Чтобы получить сведения о кодека, вызовите [**IWMHeaderInfo2:: жеткодеЦинфокаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) и [**IWMHeaderInfo2:: жеткодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) , чтобы перечислить кодеки, связанные с файлом, в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="1091f-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="1091f-129">Выберите сведения о кодека, соответствующие конфигурации потока предварительно сжатого потока.</span><span class="sxs-lookup"><span data-stu-id="1091f-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="1091f-130">Затем задайте сведения о кодека в средстве записи, вызвав [**IWMHeaderInfo3:: аддкодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), передав данные, полученные от модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="1091f-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1091f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1091f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1091f-132">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="1091f-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




