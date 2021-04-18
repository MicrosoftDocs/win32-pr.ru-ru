---
description: Для того чтобы приложение выполнило реалистичную отрисовку трехмерной сцены, оно должно учитывать эффект, который источники света оказывают на сцену.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Светлое сопоставление с текстурами (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701139"
---
# <a name="light-mapping-with-textures-direct3d-9"></a><span data-ttu-id="4158f-103">Светлое сопоставление с текстурами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4158f-103">Light Mapping with Textures (Direct3D 9)</span></span>

<span data-ttu-id="4158f-104">Для того чтобы приложение выполнило реалистичную отрисовку трехмерной сцены, оно должно учитывать эффект, который источники света оказывают на сцену.</span><span class="sxs-lookup"><span data-stu-id="4158f-104">For an application to realistically render a 3D scene, it must take into account the effect that light sources have on the appearance of the scene.</span></span> <span data-ttu-id="4158f-105">Несмотря на то что такие методы, как равномерная заливка и заливка Гуро, являются эффективными средствами в этом отношении, они могут быть недостаточными для ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="4158f-105">Although techniques such as flat and Gouraud shading are valuable tools in this respect, they can be insufficient for your needs.</span></span> <span data-ttu-id="4158f-106">Direct3D поддерживает многопроходные и множественные наложения текстуры.</span><span class="sxs-lookup"><span data-stu-id="4158f-106">Direct3D supports multipass and multiple texture blending.</span></span> <span data-ttu-id="4158f-107">Эти возможности позволяют приложению прорисовывать сцены более реалистично по сравнению с прорисовкой сцен только с помощью методов заливки.</span><span class="sxs-lookup"><span data-stu-id="4158f-107">These capabilities enable your application to render scenes with a more realistic appearance than scenes rendered with shading techniques alone.</span></span> <span data-ttu-id="4158f-108">Применяя одно или несколько сопоставлений света, ваше приложение можно разметить области света и тени на используемых в нем примитивах.</span><span class="sxs-lookup"><span data-stu-id="4158f-108">By applying one or more light maps, your application can map areas of light and shadow onto its primitives.</span></span>

<span data-ttu-id="4158f-109">Сопоставление освещения — это текстура или группа текстур, содержащая сведения об освещении в трехмерной сцене.</span><span class="sxs-lookup"><span data-stu-id="4158f-109">A light map is a texture or group of textures that contains information about lighting in a 3D scene.</span></span> <span data-ttu-id="4158f-110">Сведения об освещении можно хранить в альфа-значениях сопоставления света, в значениях цвета или в обоих этих видах значений.</span><span class="sxs-lookup"><span data-stu-id="4158f-110">You can store the lighting information in the alpha values of the light map, in the color values, or in both.</span></span>

<span data-ttu-id="4158f-111">Если вы реализуете сопоставление света с помощью многопроходного наложения текстуры, ваше приложение должно прорисовывать сопоставление света на примитивах при первом проходе.</span><span class="sxs-lookup"><span data-stu-id="4158f-111">If you implement light mapping using multipass texture blending, your application should render the light map onto its primitives on the first pass.</span></span> <span data-ttu-id="4158f-112">Второй этап следует использовать для отрисовки базовой текстуры.</span><span class="sxs-lookup"><span data-stu-id="4158f-112">It should use a second pass to render the base texture.</span></span> <span data-ttu-id="4158f-113">Исключением из этого правила является разметка отраженного света.</span><span class="sxs-lookup"><span data-stu-id="4158f-113">The exception to this is specular light mapping.</span></span> <span data-ttu-id="4158f-114">В этом случае сначала производится отрисовка базовой текстуры, а затем добавляется разметка света.</span><span class="sxs-lookup"><span data-stu-id="4158f-114">In that case, render the base texture first; then add the light map.</span></span>

<span data-ttu-id="4158f-115">Множественное наложение текстуры позволяет вашему приложению отрисовывать разметку света и базовую текстуру за один проход.</span><span class="sxs-lookup"><span data-stu-id="4158f-115">Multiple texture blending enables your application to render the light map and the base texture in one pass.</span></span> <span data-ttu-id="4158f-116">Если оборудование пользователя позволяет применять множественное наложение текстуры, ваше приложение должно использовать это преимущество при выполнении разметки освещения.</span><span class="sxs-lookup"><span data-stu-id="4158f-116">If the user's hardware provides for multiple texture blending, your application should take advantage of it when performing light mapping.</span></span> <span data-ttu-id="4158f-117">Это значительно повышает производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="4158f-117">This significantly improves your application's performance.</span></span>

<span data-ttu-id="4158f-118">С помощью сопоставления освещения приложение Direct3D может создавать разнообразные световые эффекты при отрисовке примитивов.</span><span class="sxs-lookup"><span data-stu-id="4158f-118">Using light maps, a Direct3D application can achieve a variety of lighting effects when it renders primitives.</span></span> <span data-ttu-id="4158f-119">Оно может не только размещать монохромные и цветные источники света, но также и добавлять мелкие детали, такие как блики и рассеянное освещение.</span><span class="sxs-lookup"><span data-stu-id="4158f-119">It can map not only monochrome and colored lights in a scene, but it can also add details such as specular highlights and diffuse lighting.</span></span>

<span data-ttu-id="4158f-120">Сведения об использовании наложения текстур Direct3D для создания сопоставлений освещения представлены в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="4158f-120">Information on using Direct3D texture blending to perform light mapping is presented in the following topics.</span></span>

-   [<span data-ttu-id="4158f-121">Монохромные карты светлого цвета (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4158f-121">Monochrome Light Maps (Direct3D 9)</span></span>](monochrome-light-maps.md)
-   [<span data-ttu-id="4158f-122">Карты цветового освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4158f-122">Color Light Maps (Direct3D 9)</span></span>](color-light-maps.md)
-   [<span data-ttu-id="4158f-123">Карты отраженного освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4158f-123">Specular Light Maps (Direct3D 9)</span></span>](specular-light-maps.md)
-   [<span data-ttu-id="4158f-124">Рассеянные световые карты (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4158f-124">Diffuse Light Maps (Direct3D 9)</span></span>](diffuse-light-maps.md)

## <a name="related-topics"></a><span data-ttu-id="4158f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4158f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4158f-126">Смешение текстур</span><span class="sxs-lookup"><span data-stu-id="4158f-126">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 



