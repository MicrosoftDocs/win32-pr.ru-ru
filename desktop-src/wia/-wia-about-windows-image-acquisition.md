---
description: Интерфейс Windows Image для получения изображений (WIA) — это API и интерфейс драйвера устройства (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: О приобретении образа Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711969"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="3ea71-103">О приобретении образа Windows</span><span class="sxs-lookup"><span data-stu-id="3ea71-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="3ea71-104">Интерфейс Windows Image для получения изображений (WIA) — это API и интерфейс драйвера устройства (DDI).</span><span class="sxs-lookup"><span data-stu-id="3ea71-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="3ea71-105">API-интерфейс WIA предназначен для того, чтобы приложения были:</span><span class="sxs-lookup"><span data-stu-id="3ea71-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="3ea71-106">Работа в надежной и стабильной среде.</span><span class="sxs-lookup"><span data-stu-id="3ea71-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="3ea71-107">Сократите число проблем взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="3ea71-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="3ea71-108">Перечисление доступных устройств получения изображений.</span><span class="sxs-lookup"><span data-stu-id="3ea71-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="3ea71-109">Одновременное создание подключений к нескольким устройствам.</span><span class="sxs-lookup"><span data-stu-id="3ea71-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="3ea71-110">Запрашивать свойства устройств в стандартном и расширяемом режиме.</span><span class="sxs-lookup"><span data-stu-id="3ea71-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="3ea71-111">Получение данных устройства с помощью стандартных и высокопроизводительных механизмов перемещения.</span><span class="sxs-lookup"><span data-stu-id="3ea71-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="3ea71-112">Сохранение свойств изображения при передаче данных.</span><span class="sxs-lookup"><span data-stu-id="3ea71-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="3ea71-113">Получать уведомления о различных событиях устройств.</span><span class="sxs-lookup"><span data-stu-id="3ea71-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="3ea71-114">ВИАДДИ предназначен для того, чтобы максимально увеличить объем кода, который должен написать поставщик оборудования, обеспечивая гибкость при создании отдельных решений.</span><span class="sxs-lookup"><span data-stu-id="3ea71-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="3ea71-115">Это достигается путем:</span><span class="sxs-lookup"><span data-stu-id="3ea71-115">This is accomplished by:</span></span>

-   <span data-ttu-id="3ea71-116">Предоставление стандартной библиотеки службы устройств, выполняющей большинство операций с драйверами.</span><span class="sxs-lookup"><span data-stu-id="3ea71-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="3ea71-117">Повышение стандартов связи с отраслевыми устройствами, чтобы один драйвер WIA поддерживал большинство устройств WIA.</span><span class="sxs-lookup"><span data-stu-id="3ea71-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="3ea71-118">Например, протокол (PTP).</span><span class="sxs-lookup"><span data-stu-id="3ea71-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="3ea71-119">Предоставление драйверу устройства поддержки пользовательских интерфейсов без необходимости использования стандартной библиотеки службы устройств.</span><span class="sxs-lookup"><span data-stu-id="3ea71-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="3ea71-120">Однако драйверам по-прежнему требуется реализовать стандартные интерфейсы WIA.</span><span class="sxs-lookup"><span data-stu-id="3ea71-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="3ea71-121">В этом разделе представлен краткий обзор интерфейса WIA в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="3ea71-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="3ea71-122">Архитектура WIA</span><span class="sxs-lookup"><span data-stu-id="3ea71-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="3ea71-123">Совместимость сти</span><span class="sxs-lookup"><span data-stu-id="3ea71-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="3ea71-124">Совместимость с TWAIN</span><span class="sxs-lookup"><span data-stu-id="3ea71-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="3ea71-125">диспетчер устройств WIA</span><span class="sxs-lookup"><span data-stu-id="3ea71-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="3ea71-126">Библиотека WIA Минидривер Service</span><span class="sxs-lookup"><span data-stu-id="3ea71-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="3ea71-127">WIA Минидривер</span><span class="sxs-lookup"><span data-stu-id="3ea71-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



