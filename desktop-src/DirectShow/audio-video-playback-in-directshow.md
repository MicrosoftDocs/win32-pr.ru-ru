---
description: В этом руководстве показано, как написать приложение DirectShow, которое воспроизводит файл мультимедиа.
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: Воспроизведение звука и видео в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655583"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="1f661-103">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f661-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="1f661-104">В этом руководстве показано, как написать приложение DirectShow, которое воспроизводит файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1f661-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="1f661-105">Перед прочтением этого руководства вы можете ознакомиться со следующими разделами:</span><span class="sxs-lookup"><span data-stu-id="1f661-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="1f661-106">Введение в программирование приложений DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f661-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="1f661-107">Воспроизведение файла</span><span class="sxs-lookup"><span data-stu-id="1f661-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="1f661-108">О фильтрах DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f661-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="1f661-109">О диспетчере графов фильтров</span><span class="sxs-lookup"><span data-stu-id="1f661-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="1f661-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1f661-110">In this section</span></span>

-   [<span data-ttu-id="1f661-111">Шаг 1. объявление класса Дшовплайер</span><span class="sxs-lookup"><span data-stu-id="1f661-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="1f661-112">Шаг 2. объявление Квидеорендерер и производных классов</span><span class="sxs-lookup"><span data-stu-id="1f661-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="1f661-113">Шаг 3. Создание графа фильтра</span><span class="sxs-lookup"><span data-stu-id="1f661-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="1f661-114">Шаг 4. Добавление модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="1f661-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="1f661-115">Шаг 5. Добавление функции видео</span><span class="sxs-lookup"><span data-stu-id="1f661-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="1f661-116">Шаг 6. Работа с событиями графа</span><span class="sxs-lookup"><span data-stu-id="1f661-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="1f661-117">Шаг 7. элементы управления транспорта</span><span class="sxs-lookup"><span data-stu-id="1f661-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="1f661-118">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f661-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="1f661-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1f661-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f661-120">Использование DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f661-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



