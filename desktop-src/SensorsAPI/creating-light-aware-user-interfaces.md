---
description: В этом разделе рассматривается использование данных датчика окружающей среды, а также способы оптимизации возможностей пользовательского интерфейса и содержимого программы для многих условий освещения.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Создание пользовательских интерфейсов Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999013"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="89fa5-103">Создание пользовательских интерфейсов Light-Aware</span><span class="sxs-lookup"><span data-stu-id="89fa5-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="89fa5-104">В этом разделе рассматривается использование данных датчика окружающей среды, а также способы оптимизации возможностей пользовательского интерфейса и содержимого программы для многих условий освещения.</span><span class="sxs-lookup"><span data-stu-id="89fa5-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="89fa5-105">Датчики внешнего освещения предоставляют данные, которые можно использовать для определения различных аспектов условий освещения, где расположен датчик.</span><span class="sxs-lookup"><span data-stu-id="89fa5-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="89fa5-106">Датчики внешнего освещения могут предоставлять общую яркость среды (иллуминанце) и другие аспекты окружающего освещения, такие как цветовая палитра или температура цвета.</span><span class="sxs-lookup"><span data-stu-id="89fa5-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="89fa5-107">Компьютеры могут быть более полезными несколькими способами, когда система реагирует на условия освещения.</span><span class="sxs-lookup"><span data-stu-id="89fa5-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="89fa5-108">К ним относятся: Управление яркостью компьютера (Новая, полностью поддерживаемая функция в Windows 7), автоматическая настройка уровня освещения насвеченных клавиатур и даже управление яркостью для других источников света (кнопок освещения, индикаторов активности и т. д.).</span><span class="sxs-lookup"><span data-stu-id="89fa5-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="89fa5-109">Программы для конечных пользователей также могут воспользоваться преимуществами датчиков освещения.</span><span class="sxs-lookup"><span data-stu-id="89fa5-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="89fa5-110">Программы могут применять тему, соответствующую определенному условию освещения, например определенную тему и тему.</span><span class="sxs-lookup"><span data-stu-id="89fa5-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="89fa5-111">Возможно, самым важным аспектом интеграции слабого датчика с программами являются оптимизации читаемости и читаемости, основанные на условиях освещения.</span><span class="sxs-lookup"><span data-stu-id="89fa5-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="89fa5-112">API датчика позволяет создавать такие программы.</span><span class="sxs-lookup"><span data-stu-id="89fa5-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="89fa5-113">Рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="89fa5-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="89fa5-114">Сценарий: использование ноутбука для перехода в ресторан</span><span class="sxs-lookup"><span data-stu-id="89fa5-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="89fa5-115">Предположим, вы хотите использовать компьютер для перехода к новому ресторану.</span><span class="sxs-lookup"><span data-stu-id="89fa5-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="89fa5-116">Вы начинаете с вашего дома, ищете адрес ресторана и планируете маршрут.</span><span class="sxs-lookup"><span data-stu-id="89fa5-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="89fa5-117">На следующем снимке экрана показано, как программа навигации может оптимизировать пользовательский интерфейс для отображения подробных сведений в условиях освещения.</span><span class="sxs-lookup"><span data-stu-id="89fa5-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![Пользовательский интерфейс, предназначенный для освещения.](images/nav-normal.png)

<span data-ttu-id="89fa5-119">Когда вы выходите за пределы автомобиля, вы сталкиваетесь с прямым солнечным светом, что затрудняет чтение экрана ноутбука.</span><span class="sxs-lookup"><span data-stu-id="89fa5-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="89fa5-120">На следующем снимке экрана показано, как программа может изменить пользовательский интерфейс, чтобы максимально увеличить читаемость и читаемость в прямом свете.</span><span class="sxs-lookup"><span data-stu-id="89fa5-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="89fa5-121">В этом представлении большая часть подробностей была пропущена, а контрастность — развернуто.</span><span class="sxs-lookup"><span data-stu-id="89fa5-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![Пользовательский интерфейс, предназначенный для условий прямого освещения.](images/nav-contrast.png)

<span data-ttu-id="89fa5-123">По мере приближения к ресторану мы подходим к выднему вечерам и получится темнее.</span><span class="sxs-lookup"><span data-stu-id="89fa5-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="89fa5-124">На следующем снимке экрана пользовательский интерфейс для программы навигации оптимизирован для просмотра с низким уровнем яркости.</span><span class="sxs-lookup"><span data-stu-id="89fa5-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="89fa5-125">Используя более темные цвета, этот пользовательский интерфейс легко Взгляните на самый темный автомобиль.</span><span class="sxs-lookup"><span data-stu-id="89fa5-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![Пользовательский интерфейс, предназначенный для облегчения просмотра.](images/nav-lowlight.png)

<span data-ttu-id="89fa5-127">В оставшейся части этого раздела вы узнаете о том, что можно сделать, чтобы оптимизировать программы для различных условий освещения и как использовать API датчика для включения пользовательского интерфейса с поддержкой источников.</span><span class="sxs-lookup"><span data-stu-id="89fa5-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="89fa5-128">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="89fa5-128">In This Section</span></span>

-   [<span data-ttu-id="89fa5-129">Основные принципы работы Light-Aware пользовательских интерфейсов</span><span class="sxs-lookup"><span data-stu-id="89fa5-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="89fa5-130">Примеры пользовательских интерфейсов Light-Aware</span><span class="sxs-lookup"><span data-stu-id="89fa5-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="89fa5-131">Оптимизация взаимодействия с пользователем</span><span class="sxs-lookup"><span data-stu-id="89fa5-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="89fa5-132">Основные сведения и интерпретация значений Lux</span><span class="sxs-lookup"><span data-stu-id="89fa5-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="89fa5-133">Использование данных освещения</span><span class="sxs-lookup"><span data-stu-id="89fa5-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



