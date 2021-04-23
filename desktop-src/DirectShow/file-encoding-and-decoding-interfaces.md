---
description: Интерфейсы кодирования и декодирования файлов
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Интерфейсы кодирования и декодирования файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140715"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="88612-103">Интерфейсы кодирования и декодирования файлов</span><span class="sxs-lookup"><span data-stu-id="88612-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="88612-104">Эти интерфейсы поддерживают кодирование и декодирование файлов.</span><span class="sxs-lookup"><span data-stu-id="88612-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="88612-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="88612-105">Interface</span></span>                                                    | <span data-ttu-id="88612-106">Описание</span><span class="sxs-lookup"><span data-stu-id="88612-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88612-107">**иаммедиаконтент**</span><span class="sxs-lookup"><span data-stu-id="88612-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="88612-108">Извлечение метаданных из потока, например автора и заголовка.</span><span class="sxs-lookup"><span data-stu-id="88612-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="88612-109">**иамопенпрогресс**</span><span class="sxs-lookup"><span data-stu-id="88612-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="88612-110">Определите ход выполнения операции открытия файла.</span><span class="sxs-lookup"><span data-stu-id="88612-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="88612-111">**иампарсе**</span><span class="sxs-lookup"><span data-stu-id="88612-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="88612-112">Запросите и задайте время синтаксического анализа для текущей позицией в потоке MPEG.</span><span class="sxs-lookup"><span data-stu-id="88612-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="88612-113">**иамстреамселект**</span><span class="sxs-lookup"><span data-stu-id="88612-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="88612-114">Управление воспроизведением логических потоков и получение сведений о них.</span><span class="sxs-lookup"><span data-stu-id="88612-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="88612-115">**иамвфвкомпрессдиалогс**</span><span class="sxs-lookup"><span data-stu-id="88612-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="88612-116">Отображение диалоговых окон, предоставляемых кодеками VFW.</span><span class="sxs-lookup"><span data-stu-id="88612-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="88612-117">**иамвидеокомпрессион**</span><span class="sxs-lookup"><span data-stu-id="88612-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="88612-118">Задайте параметры сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="88612-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="88612-119">**иконфигасфвритер**</span><span class="sxs-lookup"><span data-stu-id="88612-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="88612-120">Управление тем, как фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) записывает файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="88612-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="88612-121">**иконфигавимукс**</span><span class="sxs-lookup"><span data-stu-id="88612-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="88612-122">Управление процессом записи AVI файлов с помощью фильтра [мультиплексора AVI](avi-mux-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="88612-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="88612-123">**иконфигинтерлеавинг**</span><span class="sxs-lookup"><span data-stu-id="88612-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="88612-124">Настройка вывода при записи файлов AVI с помощью фильтра мультиплексора AVI.</span><span class="sxs-lookup"><span data-stu-id="88612-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="88612-125">**идвенк**</span><span class="sxs-lookup"><span data-stu-id="88612-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="88612-126">Задайте разрешение кодирования в фильтре [видео кодировщика DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="88612-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="88612-127">**идвсплиттер**</span><span class="sxs-lookup"><span data-stu-id="88612-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="88612-128">Понижение частоты кадров для цифрового видеопотока (DV)</span><span class="sxs-lookup"><span data-stu-id="88612-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="88612-129">**иипдвдек**</span><span class="sxs-lookup"><span data-stu-id="88612-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="88612-130">Задайте разрешение декодирования для фильтра [видеодекодера DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="88612-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="88612-131">**иперсистмедиапропертибаг**</span><span class="sxs-lookup"><span data-stu-id="88612-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="88612-132">Установка и получение сведений и отображаемых блоков в потоках AVI.</span><span class="sxs-lookup"><span data-stu-id="88612-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="88612-133">См. также</span><span class="sxs-lookup"><span data-stu-id="88612-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88612-134">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="88612-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



