---
title: Сведения о цветовой системе Windows версии 1.0
description: Сведения о цветовой системе Windows версии 1.0
ms.assetid: 2a162840-660e-4a66-ad16-ef3c9b07925e
keywords:
- Цветовая система Windows (WCS), сведения
- WCS (цветовая система Windows), сведения
- Управление цветом изображений, цветовая система Windows (WCS)
- Управление цветом, цветовая система Windows (WCS)
- цвета, цветовая система Windows (WCS)
- ICM (Image Color Management — управление цветом изображений)
- ICM (Управление цветом изображений)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad2673f8b0943e16a1fbbacde11c4469d00b4e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719836"
---
# <a name="about-windows-color-system-version-10"></a><span data-ttu-id="e0f88-110">Сведения о цветовой системе Windows версии 1.0</span><span class="sxs-lookup"><span data-stu-id="e0f88-110">About Windows Color System Version 1.0</span></span>

<span data-ttu-id="e0f88-111">Технология цветовой системы Microsoft Windows (WCS) обеспечивает визуализацию цветового изображения, графического или текстового объекта как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.</span><span class="sxs-lookup"><span data-stu-id="e0f88-111">Microsoft Windows Color System (WCS) technology ensures that a color image, graphic or text object is rendered as close as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="e0f88-112">Независимо от того, сканируете изображение или какой-либо рисунок на цветном сканере, скачивает его через Интернет, просматриваете или редактируете на экране или выводите его на бумагу, пленку или другие мультимедийные файлы, WCS 1,0 позволяет постоянно и точно следить за тем, чтобы цвета соответствовали.</span><span class="sxs-lookup"><span data-stu-id="e0f88-112">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it on the screen, or outputting it to paper, film, or other media, WCS 1.0 helps you keep its colors consistent and accurate.</span></span>

<span data-ttu-id="e0f88-113">WCS 1,0 является неотъемлемой частью Microsoft Windows, поскольку WCS 1,0 встроен в семейство операционных систем Windows как набор функций API Win32, он доступен для любого приложения, драйвера устройства, средства калибровки устройства или модуля управления цветом (CMM).</span><span class="sxs-lookup"><span data-stu-id="e0f88-113">WCS 1.0 is an integral part of Microsoft Windows Because WCS 1.0 is built into the Windows family of operating systems as a set of Win32 API functions, it is readily available to any application, device driver, device calibration tool, or color management module (CMM).</span></span>

<span data-ttu-id="e0f88-114">Версия 1,0 для управления цветом изображений (ICM) была предоставлена в Microsoft Windows 95 и предоставляет базовые возможности управления цветом в контекстах устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="e0f88-114">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="e0f88-115">ICM версии 2,0 входит в состав Windows 98, Windows Millennium Edition, Windows 2000 и Windows XP и включенных функций, которые реализуют управление цветом за пределами контекстов устройств.</span><span class="sxs-lookup"><span data-stu-id="e0f88-115">ICM version 2.0 is included in Windows 98, Windows Millennium Edition, Windows 2000, and Windows XP and included functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="e0f88-116">Эти функции подходят для более требовательных требований к управлению цветом и предоставляют приложениям больший контроль над процессом управления цветом.</span><span class="sxs-lookup"><span data-stu-id="e0f88-116">These functions were suitable for more demanding color management requirements, and give applications greater control over the color-management process.</span></span>

<span data-ttu-id="e0f88-117">WCS версии 1,0 входит в состав Windows Vista и включает ряд новых функций, обеспечивающих значительные улучшения в флексиблити, прозрачности, предсказуемости и расширяемости для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="e0f88-117">WCS version 1.0 is included in Windows Vista and includes a variety of new functions that provides significant improvements in flexiblity, transparency, predictability and extensiblity for vendors.</span></span>

<span data-ttu-id="e0f88-118">Какие типы приложений получат преимущество при использовании WCS 1,0?</span><span class="sxs-lookup"><span data-stu-id="e0f88-118">What kinds of applications will benefit from using WCS 1.0?</span></span> <span data-ttu-id="e0f88-119">Практически любое приложение, работающее в среде Windows Vista, уже сегодня.</span><span class="sxs-lookup"><span data-stu-id="e0f88-119">Almost any application running in a Windows Vista environment today.</span></span> <span data-ttu-id="e0f88-120">Базовая возможность управления цветом становится обязательным требованием для приложений всех типов.</span><span class="sxs-lookup"><span data-stu-id="e0f88-120">Basic color management capability is becoming a requirement for applications of all kinds.</span></span>

<span data-ttu-id="e0f88-121">Улучшение отображения и печати цвета в последние годы до момента, когда изображения с фотографией и сложная цветовая графика обычно используются не только при публикации на настольном компьютере, но и в широком спектре приложений для работы с данными и представлениями.</span><span class="sxs-lookup"><span data-stu-id="e0f88-121">Color display and printing have improved in recent years to the point where photo-realistic color images and complex color graphics are now commonly used not only in desktop publishing, but also across a broad spectrum of data and presentation applications.</span></span> <span data-ttu-id="e0f88-122">Технологии объектов, такие как COM и ActiveX, имеют внедренные объекты Color практически во всех видах пространства данных.</span><span class="sxs-lookup"><span data-stu-id="e0f88-122">Object technologies such as COM and ActiveX have embedded color objects in virtually every kind of data space.</span></span>

<span data-ttu-id="e0f88-123">Каталоги одежды, Интернет-картинки, фотоальбомы семьи, эмблемы для бизнеса, диаграммы, графики, презентации, предварительный просмотр и имитация цветов — всего лишь несколько примеров повседневных приложений, где важно иметь цвет.</span><span class="sxs-lookup"><span data-stu-id="e0f88-123">Clothing catalogs, online art, family photo albums, business logos, charts, graphs, presentations, print previews, and color simulations are just a few examples of everyday applications where color matters.</span></span>

<span data-ttu-id="e0f88-124">В результате все больше и больше пользователей требуют, чтобы их приложения могли точно отображать цвет.</span><span class="sxs-lookup"><span data-stu-id="e0f88-124">As a result, more and more users are requiring their applications to be capable of accurate color display.</span></span> <span data-ttu-id="e0f88-125">Качественная визуализация с плохими цветами руинс изображения и графики, которые все чаще важны для пользователей.</span><span class="sxs-lookup"><span data-stu-id="e0f88-125">Poor color rendering ruins the images and graphics that are increasingly important to users.</span></span>

<span data-ttu-id="e0f88-126">На базовом уровне почти любое приложение должно иметь возможность настроить цвет автоматически, чтобы на разных мониторах и принтерах его выходные данные были одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="e0f88-126">On a fundamental level, almost any application should be able to adjust color automatically so that its output looks the same on different monitors and printers.</span></span> <span data-ttu-id="e0f88-127">WCS 1,0 предоставляет набор функций для предоставления такого рода управления цветом, который является прозрачным для пользователя, и требует небольших издержек в приложении.</span><span class="sxs-lookup"><span data-stu-id="e0f88-127">WCS 1.0 provides a set of functions to deliver this kind of color management that is transparent to a user and requires little overhead in the application.</span></span>

<span data-ttu-id="e0f88-128">На более высоком уровне WCS 1,0 предоставляет дополнительные функции, обеспечивающие более сложное и управляемое управление цветом.</span><span class="sxs-lookup"><span data-stu-id="e0f88-128">On a higher level, WCS 1.0 provides additional functions that deliver more complex and controllable color management.</span></span> <span data-ttu-id="e0f88-129">Приложения для публикации графики и настольных систем потребуют этих дополнительных возможностей, чтобы пользователи могли точно работать с согласованным цветом на многих устройствах в рамках рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="e0f88-129">Graphics and desktop publishing applications need these additional capabilities to let their users work precisely with consistent color across many devices throughout a production process.</span></span>

<span data-ttu-id="e0f88-130">Как правило, производители программного обеспечения, продукты которых работают с цветными входными или выходными данными и производителями оборудования цветных периферийных устройств, найдут WCS 1,0 ключевую технологию для упрощения доставки успешных продуктов.</span><span class="sxs-lookup"><span data-stu-id="e0f88-130">In general, software vendors whose products deal with color input or output and hardware vendors of color peripherals will find WCS 1.0 a key technology for simplifying the delivery of successful products.</span></span> <span data-ttu-id="e0f88-131">Оглавление раздела:</span><span class="sxs-lookup"><span data-stu-id="e0f88-131">The following sections include:</span></span>

-   [<span data-ttu-id="e0f88-132">Новые возможности WCS версии 1.0</span><span class="sxs-lookup"><span data-stu-id="e0f88-132">What's New in Version 1.0 of WCS</span></span>](what-s-new-in-version-1-0-of-wcs.md)
-   [<span data-ttu-id="e0f88-133">Доступность WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="e0f88-133">WCS 1.0 Availability</span></span>](wcs-1-0-availability.md)

 

 




