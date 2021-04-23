---
title: Пакет SDK для Windows Media диспетчер устройств 11
description: Пакет SDK для Windows Media диспетчер устройств 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Диспетчер устройств Windows Media, сведения
- Диспетчер устройств, о программе
- Протокол передачи мультимедиа (MTP)
- MTP (протокол передачи мультимедиа)
- Класс запоминающих устройств (MSC)
- MSC (класс запоминающих устройств)
- Windows Media диспетчер устройств, классические приложения
- Диспетчер устройств, классические приложения
- Классические приложения, о
- Диспетчер устройств Windows Media, поставщики услуг
- Диспетчер устройств, поставщики услуг
- поставщики услуг, сведения
- Диспетчер устройств Windows Media, подключаемые модули
- Диспетчер устройств, Plug-инсп
- подключаемые модули, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413996"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="0d421-118">Пакет SDK для Windows Media диспетчер устройств 11</span><span class="sxs-lookup"><span data-stu-id="0d421-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d421-119">Интерфейсы API диспетчер устройств Windows Media теперь включены в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0d421-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="0d421-120">Дополнительные загрузки пакета SDK не требуются.</span><span class="sxs-lookup"><span data-stu-id="0d421-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="0d421-121">Пакет средств разработки программного обеспечения (SDK) для Microsoft Windows Media диспетчер устройств позволяет создавать настольные приложения и компоненты, которые могут взаимодействовать с подключенными портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="0d421-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="0d421-122">Windows Media диспетчер устройств позволяет приложению или компоненту выполнять перечисление, просмотр и обмен файлами с устройством, запрашивать метаданные и запрашивать сведения о количестве воспроизведений.</span><span class="sxs-lookup"><span data-stu-id="0d421-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="0d421-123">Приложения или компоненты, созданные на основе Windows Media диспетчер устройств, имеют последовательный API для взаимодействия с широким спектром устройств, включая протокол передачи мультимедиа (MTP), класс запоминающего устройства (MSC), RAPI и другие устройства, созданные на основе последних и предыдущих версий технологии Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d421-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="0d421-124">С помощью пакета SDK для диспетчер устройств Windows Media можно создать следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="0d421-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="0d421-125">Классические приложения, например пользовательские проигрыватели мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d421-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="0d421-126">Весь обмен данными между приложением и портативным устройством должен проходить через Windows Media диспетчер устройств, который выступает в качестве брокера между приложением, системой управления цифровыми правами (Майкрософт) и поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="0d421-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="0d421-127">Поставщики услуг, которые действуют как канал связи между пользовательским устройством и настольным приложением.</span><span class="sxs-lookup"><span data-stu-id="0d421-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="0d421-128">Хотя корпорация Майкрософт предоставляет несколько поставщиков услуг, которые могут обмениваться данными с большинством устройств, можно создать настраиваемый поставщик услуг для настройки связи между устройством и настольным приложением.</span><span class="sxs-lookup"><span data-stu-id="0d421-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="0d421-129">Подключаемые модули, которые могут выполнять такие задачи, как запрос и запись счетчиков воспроизведения на устройствах.</span><span class="sxs-lookup"><span data-stu-id="0d421-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="0d421-130">Эти подключаемые модули могут быть присоединены к другим классическим приложениям, таким как проигрыватель Windows Media для отправки информации поставщикам содержимого для выполнения прямых платежей исполнителям.</span><span class="sxs-lookup"><span data-stu-id="0d421-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="0d421-131">Загрузить пакет Windows Media диспетчер устройств SDK можно на [странице загрузки Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) на веб-сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="0d421-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="0d421-132">Этот пакет SDK является компонентом пакета средств разработки программного обеспечения Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d421-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="0d421-133">К другим компонентам относятся пакет SDK для Windows Media Format, пакет SDK служб Windows Media Services, пакет Windows Media Encoder SDK, пакет SDK Windows Media Rights Manager и пакет SDK проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d421-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="0d421-134">Эта документация включает в себя следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="0d421-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="0d421-135">Section</span><span class="sxs-lookup"><span data-stu-id="0d421-135">Section</span></span>                                            | <span data-ttu-id="0d421-136">Описание</span><span class="sxs-lookup"><span data-stu-id="0d421-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d421-137">Начало работы</span><span class="sxs-lookup"><span data-stu-id="0d421-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="0d421-138">Описание новых возможностей в этой версии Windows Media диспетчер устройств, а также общие сведения о работе Windows Media диспетчер устройств, описание того, что потребуется для разработки приложения или поставщика услуг, а также описание примеров, поставляемых с пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="0d421-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="0d421-139">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="0d421-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="0d421-140">Описывает, как создавать приложения и поставщики служб.</span><span class="sxs-lookup"><span data-stu-id="0d421-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="0d421-141">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="0d421-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="0d421-142">Содержит справочные сведения по C++ для интерфейсов, методов, классов и структур, поддерживаемых пакетом SDK для Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="0d421-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="0d421-143">*Глоссарий*</span><span class="sxs-lookup"><span data-stu-id="0d421-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="0d421-144">Определяет термины, используемые в этой документации.</span><span class="sxs-lookup"><span data-stu-id="0d421-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 




