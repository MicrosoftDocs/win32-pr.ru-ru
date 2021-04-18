---
title: Руководством по созданию обложки
description: Руководством по созданию обложки
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Проигрыватель Windows Media, обложки
- Обложки проигрывателя Windows Media, рекомендации по созданию
- обложки, руководством по созданию
- Создание обложек, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700539"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="b7e63-107">Руководством по созданию обложки</span><span class="sxs-lookup"><span data-stu-id="b7e63-107">Skin Creation Guide</span></span>

<span data-ttu-id="b7e63-108">Это руководство представляет собой ряд подробного объяснения того, как создавать различные виды обложек.</span><span class="sxs-lookup"><span data-stu-id="b7e63-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="b7e63-109">Более общие сведения о обложках см. в разделе [About обложки](about-skins.md).</span><span class="sxs-lookup"><span data-stu-id="b7e63-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="b7e63-110">Конкретные сведения о каждом атрибуте, методе и событии, используемом в обложках, см. в [справочнике по программированию для обложки](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b7e63-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="b7e63-111">По мере того, как вы получаете дополнительные сведения о программировании обложки, вам может потребоваться прочитать часть этого пакета SDK, охватывающую [объектную модель проигрывателя Windows Media](windows-media-player-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="b7e63-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="b7e63-112">В этом разделе приведены инструкции по созданию иллюстрации для Adobe Photoshop 5,5, популярной программы для работы с обработкой изображений.</span><span class="sxs-lookup"><span data-stu-id="b7e63-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="b7e63-113">Конкретные инструкции могут отличаться, если у вас есть похожая программа, такая как Жаск Paint Shop Pro или Sonic Found Вискосити, но основные понятия будут одинаковы.</span><span class="sxs-lookup"><span data-stu-id="b7e63-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="b7e63-114">Photoshop был выбран по двум причинам: это популярная художественная программа для коммерческих исполнителей и работает с слоями.</span><span class="sxs-lookup"><span data-stu-id="b7e63-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="b7e63-115">Как вы увидите в руководствах, слои очень полезны для создания обложки.</span><span class="sxs-lookup"><span data-stu-id="b7e63-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="b7e63-116">В этом руководством рассматриваются следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="b7e63-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="b7e63-117">Задача</span><span class="sxs-lookup"><span data-stu-id="b7e63-117">Task</span></span>                                                     | <span data-ttu-id="b7e63-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b7e63-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7e63-119">Создание первой обложки</span><span class="sxs-lookup"><span data-stu-id="b7e63-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="b7e63-120">Пошаговая простая Обложка, которая запускает и останавливает проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7e63-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="b7e63-121">Добавление списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b7e63-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="b7e63-122">Как использовать простой список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b7e63-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="b7e63-123">Выбор файлов</span><span class="sxs-lookup"><span data-stu-id="b7e63-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="b7e63-124">Выбор файлов с помощью диалогового окна «Открытие файла».</span><span class="sxs-lookup"><span data-stu-id="b7e63-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="b7e63-125">Добавление видео</span><span class="sxs-lookup"><span data-stu-id="b7e63-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="b7e63-126">Как разместить видео-окно в обложке.</span><span class="sxs-lookup"><span data-stu-id="b7e63-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="b7e63-127">Добавление визуализаций</span><span class="sxs-lookup"><span data-stu-id="b7e63-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="b7e63-128">Добавление визуализаций.</span><span class="sxs-lookup"><span data-stu-id="b7e63-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="b7e63-129">Добавление ползунка</span><span class="sxs-lookup"><span data-stu-id="b7e63-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="b7e63-130">Использование ползунка для отслеживания хода выполнения содержимого мультимедиа... и позвольте пользователю изменить его!</span><span class="sxs-lookup"><span data-stu-id="b7e63-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="b7e63-131">Создание настраиваемых ползунков</span><span class="sxs-lookup"><span data-stu-id="b7e63-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="b7e63-132">Управление томом с помощью настраиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="b7e63-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="b7e63-133">Другие примеры обложки</span><span class="sxs-lookup"><span data-stu-id="b7e63-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="b7e63-134">См. раздел Samples в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="b7e63-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="b7e63-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b7e63-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e63-136">**Обложки проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b7e63-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




