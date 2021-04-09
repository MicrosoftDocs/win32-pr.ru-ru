---
title: Считывание метаданных при воспроизведении
description: Считывание метаданных при воспроизведении
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows Media Format SDK, чтение метаданных
- Пакет SDK для Windows Media Format, асинхронный читатель
- Пакет SDK для Windows Media Format, синхронные средства чтения
- Расширенный системный формат (ASF), чтение метаданных
- ASF (Расширенный системный формат), чтение метаданных
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- асинхронные читатели, чтение метаданных
- синхронные читатели, чтение метаданных
- метаданные, чтение при воспроизведении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069686"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="c0cb2-115">Считывание метаданных при воспроизведении</span><span class="sxs-lookup"><span data-stu-id="c0cb2-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="c0cb2-116">И асинхронный, и синхронный объекты чтения могут считывать метаданные из заголовка загруженного ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="c0cb2-117">При чтении файлов атрибуты метаданных доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="c0cb2-118">Оба объекта читатель могут быть запрошены для интерфейсов [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) и [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="c0cb2-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="c0cb2-119">Дополнительные сведения о доступе к метаданным см. [в разделе Работа с метаданными](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="c0cb2-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0cb2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c0cb2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0cb2-121">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="c0cb2-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




