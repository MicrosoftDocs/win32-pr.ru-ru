---
description: Вы можете в любое время изменить звуковые графики, чтобы добавить или удалить голоса или целые вложенные диаграммы.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Руководство: динамическое добавление речи или удаление ее из звуковой схемы'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154614"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="3e393-103">Руководство: динамическое добавление речи или удаление ее из звуковой схемы</span><span class="sxs-lookup"><span data-stu-id="3e393-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="3e393-104">Вы можете в любое время изменить звуковые графики, чтобы добавить или удалить голоса или целые вложенные диаграммы.</span><span class="sxs-lookup"><span data-stu-id="3e393-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="3e393-105">В этом разделе показано, как добавить или удалить голоса субмикс из графа, созданного в результате действий из статьи Создание [базового графика обработки звука](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="3e393-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="3e393-106">Один голос может отсылать свои выходные данные нескольким голосовым или длинным цепочкам голосов.</span><span class="sxs-lookup"><span data-stu-id="3e393-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="3e393-107">Удаление или добавление одного голоса может значительно повлиять на звуковую диаграмму.</span><span class="sxs-lookup"><span data-stu-id="3e393-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="3e393-108">Динамическое изменение звуковой диаграммы</span><span class="sxs-lookup"><span data-stu-id="3e393-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="3e393-109">Добавление и удаление голосов из звуковой диаграммы очень похоже на добавление или удаление узлов из одного связанного списка или графа.</span><span class="sxs-lookup"><span data-stu-id="3e393-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="3e393-110">Добавление голоса или вложенного графа к звуковой диаграмме</span><span class="sxs-lookup"><span data-stu-id="3e393-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="3e393-111">Установите выходные данные голоса в графе, родительский Voice и голоса, которые будут добавлены с помощью функции [**сетаутпутвоицес**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) .</span><span class="sxs-lookup"><span data-stu-id="3e393-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="3e393-112">Установите выходные данные нового голоса к исходному дочернему элементу родительского голоса.</span><span class="sxs-lookup"><span data-stu-id="3e393-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="3e393-113">Удаление голоса или вложенного графа из звуковой диаграммы</span><span class="sxs-lookup"><span data-stu-id="3e393-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="3e393-114">Задайте выходной поток родительского элемента для голоса, удаляемого к дочернему элементу удаляемого голоса.</span><span class="sxs-lookup"><span data-stu-id="3e393-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="3e393-115">Если удаляемый звук находится в конце графика, родительский голосов должен быть изменен, чтобы он указывал на главный Voice.</span><span class="sxs-lookup"><span data-stu-id="3e393-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="3e393-116">Обратите внимание, что для ясности в этих примерах у каждого родителя есть только один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="3e393-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="3e393-117">Если родительский узел имеет несколько дочерних узлов, его сендлист будет содержать массив голосов вместо указателя на один голос.</span><span class="sxs-lookup"><span data-stu-id="3e393-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e393-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3e393-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e393-119">Графики воспроизведения</span><span class="sxs-lookup"><span data-stu-id="3e393-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="3e393-120">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="3e393-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="3e393-121">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="3e393-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="3e393-122">Руководство: использование субмикшированной речи</span><span class="sxs-lookup"><span data-stu-id="3e393-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="3e393-123">Руководство: создание цепи эффектов</span><span class="sxs-lookup"><span data-stu-id="3e393-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
