---
description: Зафрагментировать рамку афиши
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Зафрагментировать рамку афиши
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495774"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="3df9e-103">Зафрагментировать рамку афиши</span><span class="sxs-lookup"><span data-stu-id="3df9e-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="3df9e-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="3df9e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3df9e-105">В этой статье описывается, как отобразить кадр афиши из цифрового файла мультимедиа с помощью объекта [детектора мультимедиа (медиадет)](media-detector--mediadet.md) , поставляемого со [службами редактирования DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="3df9e-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="3df9e-106">Средство обнаружения мультимедиа — это вспомогательный объект, который может получать сведения о форматировании из исходного файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3df9e-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="3df9e-107">Он также может захватить растровое изображение из видеопотока в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="3df9e-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="3df9e-108">Предполагая, что файл доступен для поиска, можно получить образ из любой точки в файле.</span><span class="sxs-lookup"><span data-stu-id="3df9e-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="3df9e-109">Возвращаемое изображение всегда находится в 24-разрядном формате RGB.</span><span class="sxs-lookup"><span data-stu-id="3df9e-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="3df9e-110">Средство обнаружения мультимедиа не является фильтром, и приложению не требуется использовать диспетчер графов фильтров или создать граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="3df9e-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="3df9e-111">На внутреннем уровне средство обнаружения мультимедиа создает граф фильтра, содержащий [**образец фильтра захвата**](sample-grabber-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3df9e-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="3df9e-112">Чтобы получить точечный рисунок, средство обнаружения мультимедиа ищет и приостанавливает граф фильтра, а затем извлекает точечный рисунок из образца фильтра захвата.</span><span class="sxs-lookup"><span data-stu-id="3df9e-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="3df9e-113">Приложение взаимодействует с детектором мультимедиа через интерфейс [**имедиадет**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="3df9e-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="3df9e-114">Средство обнаружения мультимедийных данных — хороший пример инкапсуляции графа фильтра внутри вспомогательного объекта для экранирования приложений из сведений, относящихся к графу.</span><span class="sxs-lookup"><span data-stu-id="3df9e-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="3df9e-115">Средство обнаружения мультимедиа работает в двух режимах.</span><span class="sxs-lookup"><span data-stu-id="3df9e-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="3df9e-116">Когда вы впервые создаете его, средство обнаружения мультимедиа находится в режиме сбора информации.</span><span class="sxs-lookup"><span data-stu-id="3df9e-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="3df9e-117">Можно указать имя файла мультимедиа и получить сведения о каждом из потоков в файле, например тип формата, частоту кадров или длительность.</span><span class="sxs-lookup"><span data-stu-id="3df9e-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="3df9e-118">Если файл содержит видеопоток, можно переключить средство обнаружения мультимедиа в режим "захват растрового изображения" и получить точечные рисунки из источника.</span><span class="sxs-lookup"><span data-stu-id="3df9e-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="3df9e-119">Однако после этого вы не сможете переключить средство обнаружения мультимедиа обратно в исходный режим. Он постоянно вкладывается в этот поток видео.</span><span class="sxs-lookup"><span data-stu-id="3df9e-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="3df9e-120">Для работы с другим потоком или другим файлом необходимо создать новый экземпляр средства обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3df9e-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="3df9e-121">В примерах кода в этом руководстве используется класс ATL **CComPtr** , который автоматически управляет счетчиками ссылок.</span><span class="sxs-lookup"><span data-stu-id="3df9e-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="3df9e-122">Если вы предпочитаете использовать указатели необработанных интерфейсов, не забудьте освободить каждый интерфейс после завершения работы с ним.</span><span class="sxs-lookup"><span data-stu-id="3df9e-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="3df9e-123">Кроме того, для краткости примеры кода пропускают значительную часть проверки ошибок, которую должно выполнить приложение.</span><span class="sxs-lookup"><span data-stu-id="3df9e-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="3df9e-124">В рабочем коде всегда проверяйте значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3df9e-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="3df9e-125">Этот учебник содержит следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3df9e-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="3df9e-126">Шаг 1. Создание платформы Windows</span><span class="sxs-lookup"><span data-stu-id="3df9e-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="3df9e-127">Шаг 2. Добавление команды меню для захвата афиши</span><span class="sxs-lookup"><span data-stu-id="3df9e-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="3df9e-128">Шаг 3. Реализация функции Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="3df9e-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="3df9e-129">Шаг 4. Рисование точечного рисунка в клиентской области</span><span class="sxs-lookup"><span data-stu-id="3df9e-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="3df9e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="3df9e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3df9e-131">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="3df9e-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



