---
description: Создание графика аудиозаписи с предварительной версией
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Создание графика аудиозаписи с предварительной версией
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990291"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="3ef9c-103">Создание графика аудиозаписи с предварительной версией</span><span class="sxs-lookup"><span data-stu-id="3ef9c-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="3ef9c-104">Граф фильтра, описанный в разделе [Создание графика записи звука](creating-an-audio-capture-graph.md) , выполняет только захват без предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="3ef9c-105">Для предварительного просмотра и записи на диаграмме фильтра необходимо использовать [Фильтр неограниченный ПИН-код tee](infinite-pin-tee-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3ef9c-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="3ef9c-106">Этот фильтр имеет один входной ПИН-код и при необходимости создает столько выходных контактов.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="3ef9c-107">(Он начинается с одного выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-107">(It starts with one output pin.</span></span> <span data-ttu-id="3ef9c-108">Каждый раз при подключении выходного ПИН-кода создается еще один.) Фильтр неограниченного ПИН-кода tee обеспечивает каждый полученный пример, без изменений, через все его выходные сигналы.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="3ef9c-109">Подключите фильтр записи звука к бесконечному ПИН-tee и подключите неограниченный ПИН-код tee к мультиплексору и [фильтру модуля обработки DirectSound](directsound-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3ef9c-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="3ef9c-110">Подключите мультиплексор к модулю записи файлов, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="3ef9c-111">На следующей схеме показан итоговый граф фильтра для файла AVI.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![Диаграмма записи звука с предварительной версией](images/audio-capture-graph.png)

<span data-ttu-id="3ef9c-113">Так как модуль подготовки DirectSound является модулем подготовки звука по умолчанию, можно просто вызвать метод [**играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) для выходного контакта Tee с бесконечным ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="3ef9c-114">Диспетчер графов фильтров использует [интеллектуальное соединение](intelligent-connect.md) для создания модуля подготовки отчетов, добавления его в граф фильтра и подключения к контактам.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="3ef9c-115">Если вы захватываете звук с микрофона и проводите его с докладчика на том же компьютере, вы можете создать отзыв о звуках.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3ef9c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3ef9c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ef9c-117">Запись звука</span><span class="sxs-lookup"><span data-stu-id="3ef9c-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



