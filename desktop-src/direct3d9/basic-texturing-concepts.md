---
description: Ранние созданные на компьютере трехмерные изображения, как правило, имели глянцевый, "пластиковый" вид, несмотря на то что были достаточно продвинутыми для своего времени.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Основные понятия текстурирования (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692028"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="aa8df-103">Основные понятия текстурирования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aa8df-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="aa8df-104">Ранние созданные на компьютере трехмерные изображения, как правило, имели глянцевый, "пластиковый" вид, несмотря на то что были достаточно продвинутыми для своего времени.</span><span class="sxs-lookup"><span data-stu-id="aa8df-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="aa8df-105">В них отсутствовали разнообразные типы маркировки, такие как царапины, трещины, отпечатки пальцев и пятна, придающие трехмерным объектам реалистичную визуальную сложность.</span><span class="sxs-lookup"><span data-stu-id="aa8df-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="aa8df-106">В последние годы текстуры получают популярность от разработчиков в качестве средства для улучшения реальных трехмерных изображений, созданных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="aa8df-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="aa8df-107">В повседневном использовании слово "текстура" используется для обозначения гладкости или шероховатости объекта.</span><span class="sxs-lookup"><span data-stu-id="aa8df-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="aa8df-108">Однако в компьютерной графике текстура — это точечный рисунок пиксельных цветов, придающих объекту внешний вид текстуры.</span><span class="sxs-lookup"><span data-stu-id="aa8df-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="aa8df-109">Поскольку текстуры Direct3D — это точечные рисунки, к примитиву Direct3D может быть применен любой точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="aa8df-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="aa8df-110">Например, приложения могут создавать объекты, которые выглядят, как будто имеют узор древесной структуры, и выполнять с ними различные операции.</span><span class="sxs-lookup"><span data-stu-id="aa8df-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="aa8df-111">К набору трехмерных примитивов, образующих холм, можно добавить траву, грязь и камни.</span><span class="sxs-lookup"><span data-stu-id="aa8df-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="aa8df-112">В результате мы получим выглядящий весьма реалистично склон холма.</span><span class="sxs-lookup"><span data-stu-id="aa8df-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="aa8df-113">Кроме того, текстурирование можно использовать для создания эффектов, таких как знаки на обочине дороги, горные пласты в ущелье или мрамор на полу.</span><span class="sxs-lookup"><span data-stu-id="aa8df-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="aa8df-114">Кроме того, Direct3D поддерживает более сложные техники текстурирования, такие как наложение текстур с прозрачностью и без и сопоставление света.</span><span class="sxs-lookup"><span data-stu-id="aa8df-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="aa8df-115">Дополнительные сведения см. в статьях [смешение текстур (Direct3D 9)](texture-blending.md) и [светлое сопоставление с текстурами (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="aa8df-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="aa8df-116">Если ваше приложение создает устройство слоя абстрагирования оборудования (HAL) или программное устройство, оно может использовать 8-, 16-, 24-, 32-, 64- или 128-разрядные текстуры.</span><span class="sxs-lookup"><span data-stu-id="aa8df-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="aa8df-117">Дополнительные сведения содержатся в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="aa8df-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="aa8df-118">Режимы адресации текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aa8df-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="aa8df-119">Изменившиеся регионы текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aa8df-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="aa8df-120">Палитры текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aa8df-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="aa8df-121">См. также</span><span class="sxs-lookup"><span data-stu-id="aa8df-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa8df-122">Текстуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="aa8df-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



