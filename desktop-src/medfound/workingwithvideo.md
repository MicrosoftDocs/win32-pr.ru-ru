---
description: Работа с видео
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: Работа с видео (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348725"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="17077-103">Работа с видео (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="17077-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="17077-104">Хотя отдельные видеокодеки имеют собственный странностой, все они используют одни и те же базовые процедуры.</span><span class="sxs-lookup"><span data-stu-id="17077-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="17077-105">В этом разделе описывается, как кодировать и декодировать видео с помощью видеокодеков Windows Media и устранить конкретные функции каждого из них.</span><span class="sxs-lookup"><span data-stu-id="17077-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="17077-106">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="17077-106">This section contains the following topics.</span></span>



| <span data-ttu-id="17077-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="17077-107">Topic</span></span>                                                                                                        | <span data-ttu-id="17077-108">Описание</span><span class="sxs-lookup"><span data-stu-id="17077-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17077-109">Выбор видеокодека</span><span class="sxs-lookup"><span data-stu-id="17077-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="17077-110">Описывает типы содержимого, которые лучше всего подходят для сжатия, с помощью видеокодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="17077-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="17077-111">Настройка кодирования видео</span><span class="sxs-lookup"><span data-stu-id="17077-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="17077-112">Описание настройки дмос кодировщика видео.</span><span class="sxs-lookup"><span data-stu-id="17077-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="17077-113">Настройка декодирования видео</span><span class="sxs-lookup"><span data-stu-id="17077-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="17077-114">Описание настройки видеодекодера дмос.</span><span class="sxs-lookup"><span data-stu-id="17077-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="17077-115">Принудительная вставка ключевых кадров</span><span class="sxs-lookup"><span data-stu-id="17077-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="17077-116">Описывает, как запросить кодирование образца в качестве ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="17077-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="17077-117">Кодирование видео с чередованием</span><span class="sxs-lookup"><span data-stu-id="17077-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="17077-118">Описывает, как сохранить чередование в потоках видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="17077-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="17077-119">Использование кодека расширенного профиля Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="17077-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="17077-120">Описывает использование кодека расширенного профиля Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="17077-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="17077-121">Использование экранного видеокодека Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="17077-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="17077-122">Описывает, как использовать экранный кодек Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="17077-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="17077-123">Использование кодека образа Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="17077-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="17077-124">Описывает использование кодека образа Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="17077-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="17077-125">См. также</span><span class="sxs-lookup"><span data-stu-id="17077-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17077-126">Кодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="17077-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



