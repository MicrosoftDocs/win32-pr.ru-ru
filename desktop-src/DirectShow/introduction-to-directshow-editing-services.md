---
description: Введение в службы редактирования DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Введение в службы редактирования DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494964"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="df2ea-103">Введение в службы редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="df2ea-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="df2ea-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="df2ea-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="df2ea-105">Основой DirectShow является мощная архитектура для обработки потокового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="df2ea-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="df2ea-106">Приложение может использовать его для воспроизведения мультимедийного содержимого, созданного в широком спектре форматов, не требуя от разработчика необходимости беспокоиться о сжатии файлов и других утомительных деталях.</span><span class="sxs-lookup"><span data-stu-id="df2ea-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="df2ea-107">Однако до [служб редактирования DirectShow](directshow-editing-services.md) (DES) в DirectShow отсутствовала гибкость, необходимая для нелинейного редактирования.</span><span class="sxs-lookup"><span data-stu-id="df2ea-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="df2ea-108">Например, предположим, что вы решили создать видеопоследовательность, состоящую из 4 секунд от источника A, за которой следуют 10 секунд от источника б и заканчивается 5 секунд из источника C. Это можно сделать гораздо проще, используя только базовый API DirectShow.</span><span class="sxs-lookup"><span data-stu-id="df2ea-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="df2ea-109">Но что делать, если вы решили, что исходный C должен следовать перед источником B, а не после; в этом случае в последовательности должно использоваться 8 секунд от источника A, а не 4; и что для всего производства требуется отдельная звуковая дорожка в фоновом режиме?</span><span class="sxs-lookup"><span data-stu-id="df2ea-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="df2ea-110">Даже небольшие изменения, например, могут быть трудно реализовать.</span><span class="sxs-lookup"><span data-stu-id="df2ea-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="df2ea-111">Но описанный сценарий является тривиальным проектом редактирования в DES — вы можете сделать это с помощью нескольких вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="df2ea-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="df2ea-112">Ниже приведены некоторые функции, которые DES переносит в DirectShow:</span><span class="sxs-lookup"><span data-stu-id="df2ea-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="df2ea-113">Модель временной шкалы, которая организует видео-и звуковые дорожки во вложенные слои, что упрощает работу с окончательным производством.</span><span class="sxs-lookup"><span data-stu-id="df2ea-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="df2ea-114">Возможность предварительного просмотра видео-проекта в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="df2ea-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="df2ea-115">Сохранение проекта с помощью формата на основе XML</span><span class="sxs-lookup"><span data-stu-id="df2ea-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="df2ea-116">Поддержка видео-и звуковых эффектов, а также переходы между видеодорожками (например, исчезание и стирание)</span><span class="sxs-lookup"><span data-stu-id="df2ea-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="df2ea-117">Более 100 стандартных стираниех, как определено обществом инженеров движения и телевизионных специалистов (SMPTE)</span><span class="sxs-lookup"><span data-stu-id="df2ea-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="df2ea-118">Ключ, основанный на оттенках, освещенности, значении RGB или альфа-значении</span><span class="sxs-lookup"><span data-stu-id="df2ea-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="df2ea-119">Автоматическое преобразование частот кадров и частот дискретизации, что позволяет рабочей среде использовать разнородные источники</span><span class="sxs-lookup"><span data-stu-id="df2ea-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="df2ea-120">Изменение размера или обрезка видео</span><span class="sxs-lookup"><span data-stu-id="df2ea-120">Resizing or cropping of video</span></span>

<span data-ttu-id="df2ea-121">Ограничения</span><span class="sxs-lookup"><span data-stu-id="df2ea-121">Limitations:</span></span>

-   <span data-ttu-id="df2ea-122">DES не поддерживает источники видео MPEG-2 или H. 264.</span><span class="sxs-lookup"><span data-stu-id="df2ea-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df2ea-123">См. также</span><span class="sxs-lookup"><span data-stu-id="df2ea-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df2ea-124">Службы редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="df2ea-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



