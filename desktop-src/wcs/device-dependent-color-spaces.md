---
title: Аппаратно-зависимые цветовые пространства
description: Большинство цветовых пространств зависит от устройства.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Цветовая система Windows (WCS), аппаратно-зависимые цветовые пространства
- WCS (цветовая система Windows), аппаратно-зависимые цветовые пространства
- Управление цветом изображений, аппаратно-зависимые цветовые пространства
- Управление цветом, аппаратно-зависимые цветовые пространства
- цвета, аппаратно-зависимые цветовые пространства
- цветовые пространства, зависящие от устройства
- аппаратно-зависимые цветовые пространства
- Белая точка
- колорантс
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719823"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="8dd07-112">Аппаратно-зависимые цветовые пространства</span><span class="sxs-lookup"><span data-stu-id="8dd07-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="8dd07-113">Большинство [цветовых пространств](c.md) зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="8dd07-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="8dd07-114">Хотя конкретное устройство, например принтер, может использовать цветовое пространство CMYK, цвета, отображаемые для определенных значений CMYK, часто немного отличаются от других типов принтеров.</span><span class="sxs-lookup"><span data-stu-id="8dd07-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="8dd07-115">Именно по этой причине система управления цветом WCS 1,0 настолько полезна.</span><span class="sxs-lookup"><span data-stu-id="8dd07-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="8dd07-116">Все цветовые пространства имеют *белую точку*, которая определяется как белый квадрат, который может быть создан в этом цветовом пространстве.</span><span class="sxs-lookup"><span data-stu-id="8dd07-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="8dd07-117">Так как устройства могут отличаться друг от друга, их белые точки также могут различаться.</span><span class="sxs-lookup"><span data-stu-id="8dd07-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="8dd07-118">Все цвета, которые может создавать устройство, зависят от его белого пункта.</span><span class="sxs-lookup"><span data-stu-id="8dd07-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="8dd07-119">Таким образом, система управления цветом должна иметь возможность сопоставлять белую точку одного цветового пространства с другим и сохранять относительные расположения всех цветов.</span><span class="sxs-lookup"><span data-stu-id="8dd07-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="8dd07-120">Он также должен иметь возможность сопоставить цвет в одном цветовом пространстве с ближайшим совпадением в другом цветном пространстве независимо от различий в белой точке.</span><span class="sxs-lookup"><span data-stu-id="8dd07-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="8dd07-121">WCS 1,0 может выполнять обе эти задачи.</span><span class="sxs-lookup"><span data-stu-id="8dd07-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="8dd07-122">Цветовое пространство RGB часто используется на мониторах компьютеров.</span><span class="sxs-lookup"><span data-stu-id="8dd07-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="8dd07-123">Таким образом, это зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="8dd07-123">As such, it is device dependent.</span></span> <span data-ttu-id="8dd07-124">Принтеры обычно используют CMYK [колорантс](c.md).</span><span class="sxs-lookup"><span data-stu-id="8dd07-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="8dd07-125">Каждый принтер реализует собственную версию цветового пространства CMYK.</span><span class="sxs-lookup"><span data-stu-id="8dd07-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="8dd07-126">Цифровые изображения могут не хранить цвета в них.</span><span class="sxs-lookup"><span data-stu-id="8dd07-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="8dd07-127">Они могут хранить номера индексов в палитре цветов.</span><span class="sxs-lookup"><span data-stu-id="8dd07-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="8dd07-128">В результате разработчики отдельных приложений очень трудно использовать или предоставить стандартизированный метод перемещения цветовых изображений с одного устройства на другое.</span><span class="sxs-lookup"><span data-stu-id="8dd07-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="8dd07-129">Специалисты по созданию образов обычно испытывают недовольство при создании графического изображения на экране компьютера и при его печати сильно отличаются.</span><span class="sxs-lookup"><span data-stu-id="8dd07-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="8dd07-130">WCS 1,0 устраняет эти потребности в образах.</span><span class="sxs-lookup"><span data-stu-id="8dd07-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




