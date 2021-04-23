---
title: Метафайлы Windows Media
description: Метафайлы Windows Media
ms.assetid: 77af7d15-52ac-496c-8037-51827adf0250
keywords:
- Метафайлы Windows Media, сведения
- Проигрыватель Windows Media, метафайлы
- Проигрыватель Windows Media, метафайлы Windows Media
- Метафайлы, сведения
- Windows Media, метафайлы
- Списки воспроизведения метафайлов Windows Media, сведения
- списки воспроизведения, сведения
- списки воспроизведения метафайлов, сведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 385b149e07e9d30df4e11a21f8e7aa4b05e06910
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330051"
---
# <a name="windows-media-metafiles"></a><span data-ttu-id="a6e41-111">Метафайлы Windows Media</span><span class="sxs-lookup"><span data-stu-id="a6e41-111">Windows Media Metafiles</span></span>

<span data-ttu-id="a6e41-112">В этой справочной документации описываются метафайлы Windows Media, которые используют расширения имен файлов. мастика,. ввкс,. ВМКС и. ASX.</span><span class="sxs-lookup"><span data-stu-id="a6e41-112">This reference documents Windows Media metafiles, which use the .wax, .wvx, .wmx, and .asx file name extensions.</span></span> <span data-ttu-id="a6e41-113">В нем содержатся общие сведения и разделы руководств по программированию, а также полный справочный раздел по тегам элементов метафайлов, их атрибутам и значениям, а также специальным условиям, связанным с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="a6e41-113">It contains overview and programming guide sections, and a full reference section on metafile element tags, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="a6e41-114">Метафайл — это файл, содержащий сведения о других файлах.</span><span class="sxs-lookup"><span data-stu-id="a6e41-114">A metafile is a file that contains information about other files.</span></span> <span data-ttu-id="a6e41-115">Метафайл можно использовать для вывода списка файлов мультимедийного содержимого, которые будут воспроизводиться по порядку.</span><span class="sxs-lookup"><span data-stu-id="a6e41-115">A metafile can be used to list a group of media content files that are to be played in order.</span></span> <span data-ttu-id="a6e41-116">Списки воспроизведения метафайлов Windows Media, которые просто называются списками воспроизведения в этом справочном документе, являются одной из самых эффективных функций технологий Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a6e41-116">Windows Media metafile playlists, simply referred to as playlists in this reference document, are one of the most powerful features of Microsoft Windows Media Technologies.</span></span> <span data-ttu-id="a6e41-117">Списки воспроизведения позволяют управлять содержимым мультимедиа и настраивать его.</span><span class="sxs-lookup"><span data-stu-id="a6e41-117">Playlists allow you to control and customize your media content.</span></span> <span data-ttu-id="a6e41-118">Например, с помощью списков воспроизведения можно запланировать воспроизведение содержимого в случае успеха или вставить рекламные или специальные клипы в презентацию.</span><span class="sxs-lookup"><span data-stu-id="a6e41-118">For instance, with playlists you can schedule content to play in succession or insert advertising or special interest clips into a presentation.</span></span> <span data-ttu-id="a6e41-119">Еще одним преимуществом списков воспроизведения является то, что вместо воспроизведения потока, остановки, запуска следующего потока и последующего ожидания завершения работы буферизации службы Windows Media и проигрыватель Windows Media работают вместе, чтобы воспроизвести клипы один за другим с минимальным временем буферизации или перерывом между ними.</span><span class="sxs-lookup"><span data-stu-id="a6e41-119">A further advantage of playlists is that instead of playing a stream, stopping, starting the next stream, and then waiting for it to finish buffering, Windows Media Services and Windows Media Player work together to play the clips one after the other with minimal buffering time or interruption between them.</span></span>

<span data-ttu-id="a6e41-120">Технологии Windows Media и другие Интернет-продукты предоставляют средства для понимания демографических пользователей и динамического настройки вещания или сообщения для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="a6e41-120">Windows Media Technologies and other Internet products provide you with the tools to understand user demographics and dynamically customize a broadcast or message for individual users.</span></span>

<span data-ttu-id="a6e41-121">Этот справочник разделен на следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="a6e41-121">This reference is divided into the following sections.</span></span>



| <span data-ttu-id="a6e41-122">Section</span><span class="sxs-lookup"><span data-stu-id="a6e41-122">Section</span></span>                                                                  | <span data-ttu-id="a6e41-123">Описание</span><span class="sxs-lookup"><span data-stu-id="a6e41-123">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6e41-124">О метафайлах Windows Media</span><span class="sxs-lookup"><span data-stu-id="a6e41-124">About Windows Media Metafiles</span></span>](about-windows-media-metafiles.md)       | <span data-ttu-id="a6e41-125">Представляет элементы метафайлов Windows Media и обсуждает их назначение.</span><span class="sxs-lookup"><span data-stu-id="a6e41-125">Introduces Windows Media metafile elements and discusses their purpose.</span></span>                                                                                                             |
| [<span data-ttu-id="a6e41-126">Путеводитель по метафайлу Windows Media</span><span class="sxs-lookup"><span data-stu-id="a6e41-126">Windows Media Metafile Guide</span></span>](windows-media-metafile-guide.md)         | <span data-ttu-id="a6e41-127">Подробное описание действий, необходимых для создания метафайлов.</span><span class="sxs-lookup"><span data-stu-id="a6e41-127">Details the steps necessary for creating metafiles.</span></span> <span data-ttu-id="a6e41-128">Примеры иллюстрируют использование тегов элементов для конкретных задач.</span><span class="sxs-lookup"><span data-stu-id="a6e41-128">Examples illustrate how to use element tags for specific tasks.</span></span>                                                                 |
| [<span data-ttu-id="a6e41-129">Справочник по метафайлу Windows Media</span><span class="sxs-lookup"><span data-stu-id="a6e41-129">Windows Media Metafile Reference</span></span>](windows-media-metafile-reference.md) | <span data-ttu-id="a6e41-130">Подробное описание каждого из элементов метафайла, их атрибутов и значений, а также специальных условий, связанных с каждым из них.</span><span class="sxs-lookup"><span data-stu-id="a6e41-130">Explains in detail each of the metafile elements, their attributes and values, and special conditions related to each.</span></span> <span data-ttu-id="a6e41-131">Описывает расширения метафайлов имен файлов и их правильное использование.</span><span class="sxs-lookup"><span data-stu-id="a6e41-131">Explains metafile file name extensions and their proper use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a6e41-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a6e41-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6e41-133">**Пакет SDK для проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a6e41-133">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




