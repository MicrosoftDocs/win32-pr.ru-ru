---
title: Отобразить подключаемые модули области (не рекомендуется)
description: Отобразить подключаемые модули области (не рекомендуется)
ms.assetid: 424e6f9b-3ecf-4172-9eb9-cd2ac532b488
keywords:
- Подключаемые модули проигрывателя Windows Media, область экрана
- подключаемые модули, область экрана
- подключаемые модули пользовательского интерфейса, область экрана
- Подключаемые модули пользовательского интерфейса, область экрана
- подключаемые модули области дисплея
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb398d4c0a1c0886183f4d6213874e4e54656965
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411438"
---
# <a name="display-area-plug-ins-deprecated"></a><span data-ttu-id="e9982-108">Отобразить подключаемые модули области (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="e9982-108">Display Area Plug-ins (deprecated)</span></span>

<span data-ttu-id="e9982-109">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="e9982-109">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="e9982-110">Подключаемые модули пользовательского интерфейса области отображения отображаются в основной области области **Воспроизведение** под названием исполнителя и сведения о дорожке, а также слева от области списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e9982-110">Display area UI plug-ins are shown in the main area of the **Now Playing** pane, below the artist and track information and to the left of the playlist area.</span></span> <span data-ttu-id="e9982-111">В каждый момент времени может быть включен только один подключаемый модуль экранной области.</span><span class="sxs-lookup"><span data-stu-id="e9982-111">Only one display area plug-in can be enabled at a time.</span></span> <span data-ttu-id="e9982-112">Если подключаемый модуль области отображения включен, проигрыватель не может перейти в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="e9982-112">When a display area plug-in is enabled, the Player cannot enter full screen mode.</span></span>

<span data-ttu-id="e9982-113">Подключаемые модули области отображения полезны для отображения больших объемов информации.</span><span class="sxs-lookup"><span data-stu-id="e9982-113">Display area plug-ins are useful for displaying large amounts of information.</span></span> <span data-ttu-id="e9982-114">Например, подключаемый модуль области просмотра может получать сведения о воспроизводимом в данный момент элементе мультимедиа и отображать связанные статьи, интервью и обзоры.</span><span class="sxs-lookup"><span data-stu-id="e9982-114">For example, a display area plug-in can retrieve information about the currently playing media item and display related articles, interviews, and reviews.</span></span> <span data-ttu-id="e9982-115">Подключаемый модуль области просмотра может содержать окно браузера Microsoft Internet Explorer для вывода этих сведений с помощью HTML.</span><span class="sxs-lookup"><span data-stu-id="e9982-115">A display area plug-in can host a Microsoft Internet Explorer browser window to display this information using HTML.</span></span>

> [!Note]  
> <span data-ttu-id="e9982-116">Размещенное окно браузера может внедрять версию ActiveX проигрывателя Windows Media, но это не рекомендуется, поскольку внедренный элемент управления не может взаимодействовать с автономным проигрывателем, содержащим его.</span><span class="sxs-lookup"><span data-stu-id="e9982-116">A hosted browser window can embed the ActiveX version of Windows Media Player, but this is not recommended because the embedded control cannot communicate with the standalone player that contains it.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9982-117">Проигрыватель Windows Media закрывает любой открытый подключаемый модуль области экрана, когда пользователь воспроизводит содержимое, содержащее видео.</span><span class="sxs-lookup"><span data-stu-id="e9982-117">Windows Media Player closes any open display area plug-in when the user plays content that contains video.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e9982-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e9982-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9982-119">**Общие сведения о подключаемом модуле пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="e9982-119">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




