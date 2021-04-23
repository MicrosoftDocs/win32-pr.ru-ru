---
description: При создании трехмерных сцен приложение иногда может повысить производительность, выполнив визуализацию 2D-объектов таким образом, чтобы они отображались как трехмерные объекты. Это основная идея для методики объявления.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Объявление (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701291"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="529d5-104">Объявление (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="529d5-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="529d5-105">При создании трехмерных сцен приложение иногда может повысить производительность, выполнив визуализацию 2D-объектов таким образом, чтобы они отображались как трехмерные объекты.</span><span class="sxs-lookup"><span data-stu-id="529d5-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="529d5-106">Это основная идея для методики объявления.</span><span class="sxs-lookup"><span data-stu-id="529d5-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="529d5-107">Объявление в нормальном смысле слова является знаком по роадвай.</span><span class="sxs-lookup"><span data-stu-id="529d5-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="529d5-108">Приложения Microsoft Direct3D могут создавать и визуализировать этот тип рекламы, определяя прямоугольную заливку и применяя к ней текстуру.</span><span class="sxs-lookup"><span data-stu-id="529d5-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="529d5-109">Объявление в более специализированном смысле трехмерной графики является расширением этого.</span><span class="sxs-lookup"><span data-stu-id="529d5-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="529d5-110">Цель состоит в том, чтобы сделать двумерные объекты трехмерными.</span><span class="sxs-lookup"><span data-stu-id="529d5-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="529d5-111">Метод — применить текстуру, которая содержит изображение объекта, к прямоугольному примитиву.</span><span class="sxs-lookup"><span data-stu-id="529d5-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="529d5-112">Примитив поворачивается таким образом, чтобы он всегда был лицевым пользователем.</span><span class="sxs-lookup"><span data-stu-id="529d5-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="529d5-113">Не имеет значения, является ли изображение объекта прямоугольным.</span><span class="sxs-lookup"><span data-stu-id="529d5-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="529d5-114">Части объявления можно сделать прозрачными, поэтому части изображения объявления, которые вы не хотите видеть, не видны.</span><span class="sxs-lookup"><span data-stu-id="529d5-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="529d5-115">Во многих играх используются объявления для анимационных спрайтов.</span><span class="sxs-lookup"><span data-stu-id="529d5-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="529d5-116">Например, когда пользователь перемещается по трехмерному лабиринту, он может видеть оружие или вознаграждения, которые могут быть получены.</span><span class="sxs-lookup"><span data-stu-id="529d5-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="529d5-117">Обычно это 2D-изображения, которые текстурированы на прямоугольном примитиве.</span><span class="sxs-lookup"><span data-stu-id="529d5-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="529d5-118">Объявления часто используются в играх для отрисовки изображений деревьев, бушес и облаков.</span><span class="sxs-lookup"><span data-stu-id="529d5-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="529d5-119">При применении изображения к рекламному стенду необходимо сначала повернуть прямоугольный примитив, чтобы полученное изображение было направлено пользователю.</span><span class="sxs-lookup"><span data-stu-id="529d5-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="529d5-120">Приложение должно перевести его в нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="529d5-120">Your application must then translate it into position.</span></span> <span data-ttu-id="529d5-121">Затем приложение может применить к примитиву текстуру.</span><span class="sxs-lookup"><span data-stu-id="529d5-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="529d5-122">Объявления лучше всего подходят для симметричных объектов, особенно для объектов, симметричных вдоль вертикальной оси.</span><span class="sxs-lookup"><span data-stu-id="529d5-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="529d5-123">Также требуется, чтобы высота точки зрения не слишком велика.</span><span class="sxs-lookup"><span data-stu-id="529d5-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="529d5-124">Если пользователю разрешено просматривать рекламу, объявленную выше, она становится очевидной, что объект является 2D, а не трехмерным.</span><span class="sxs-lookup"><span data-stu-id="529d5-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="529d5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="529d5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="529d5-126">Примеры альфа</span><span class="sxs-lookup"><span data-stu-id="529d5-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



