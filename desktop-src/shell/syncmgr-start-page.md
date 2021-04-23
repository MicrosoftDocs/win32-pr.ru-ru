---
description: Диспетчер синхронизации предоставляет централизованную, стандартную технологию для синхронизации файлов для автономного использования на мобильном компьютере или на компьютере, подключенном к локальной сети.
title: диспетчер синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997759"
---
# <a name="synchronization-manager"></a><span data-ttu-id="de8b4-103">диспетчер синхронизации</span><span class="sxs-lookup"><span data-stu-id="de8b4-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="de8b4-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="de8b4-104">Purpose</span></span>

<span data-ttu-id="de8b4-105">Диспетчер синхронизации предоставляет централизованную, стандартную технологию для синхронизации файлов для автономного использования на мобильном компьютере или на компьютере, подключенном к локальной сети.</span><span class="sxs-lookup"><span data-stu-id="de8b4-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="de8b4-106">Вместе с функциями подключения, уведомлениями (служба уведомлений о системных событиях) и кэшированием на стороне клиента диспетчер синхронизации предоставляет инфраструктуру для поддержки мобильных вычислений.</span><span class="sxs-lookup"><span data-stu-id="de8b4-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="de8b4-107">Вместо каждого приложения, реализующего собственные технологии для кэширования и синхронизации сетевых ресурсов для локального использования, операционная система предоставляет интегрированную модель, которую могут использовать все приложения.</span><span class="sxs-lookup"><span data-stu-id="de8b4-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="de8b4-108">Файлы синхронизируются независимо от протокола.</span><span class="sxs-lookup"><span data-stu-id="de8b4-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="de8b4-109">Например, программа электронной почты может передавать свои сообщения с помощью протокола SMTP, НМТП или POP3, в то время как браузер может использовать протокол HTTP, а база данных может использовать удаленный вызов процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="de8b4-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="de8b4-110">Разработчики могут использовать общий интерфейс диспетчера синхронизации в своих приложениях для синхронизации файлов между локальным компьютером пользователя и сетевым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="de8b4-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="de8b4-111">Где применимо</span><span class="sxs-lookup"><span data-stu-id="de8b4-111">Where applicable</span></span>

<span data-ttu-id="de8b4-112">Диспетчер синхронизации предназначен для приложений, которые работают в основном на мобильных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="de8b4-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="de8b4-113">Использование диспетчера синхронизации для приложений, работающих на компьютерах, подключенных к локальным сетям с высокой задержкой, может также оказаться выгодным.</span><span class="sxs-lookup"><span data-stu-id="de8b4-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="de8b4-114">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="de8b4-114">Developer audience</span></span>

<span data-ttu-id="de8b4-115">Этот документ предназначен для разработчиков программного обеспечения, разрабатывающих приложения для мобильных вычислений и локальных сетей с высокой задержкой.</span><span class="sxs-lookup"><span data-stu-id="de8b4-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="de8b4-116">Этот документ содержит полный справочник по всем частям диспетчера синхронизации, включая методы и интерфейсы для диспетчера синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de8b4-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="de8b4-117">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="de8b4-117">Run-time requirements</span></span>

<span data-ttu-id="de8b4-118">Требуется Windows Server 2003, Windows XP, Windows 2000 или Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="de8b4-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="de8b4-119">Также доступна в качестве распространяемого пакета для Microsoft Windows NT 4,0, Windows 98 и Windows 95.</span><span class="sxs-lookup"><span data-stu-id="de8b4-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de8b4-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="de8b4-120">In this section</span></span>



| <span data-ttu-id="de8b4-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="de8b4-121">Topic</span></span>                                                                                       | <span data-ttu-id="de8b4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="de8b4-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de8b4-123">О диспетчере синхронизации</span><span class="sxs-lookup"><span data-stu-id="de8b4-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="de8b4-124">Диспетчер синхронизации предоставляет централизованную, стандартную технологию для синхронизации файлов для автономного использования на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="de8b4-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="de8b4-125">Конфигурации мобильных вычислений</span><span class="sxs-lookup"><span data-stu-id="de8b4-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="de8b4-126">Приложения могут использовать синхронизации Manager для сохранения кэширования файлов и ресурсов в локальной среде и синхронизации на мобильных и настольных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="de8b4-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="de8b4-127">Сценарии приложений</span><span class="sxs-lookup"><span data-stu-id="de8b4-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="de8b4-128">Приложения и службы, которые могут использовать диспетчер синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de8b4-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="de8b4-129">Архитектура диспетчера синхронизации</span><span class="sxs-lookup"><span data-stu-id="de8b4-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="de8b4-130">Использование диспетчера синхронизации из программы</span><span class="sxs-lookup"><span data-stu-id="de8b4-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="de8b4-131">Справочник по диспетчеру синхронизации</span><span class="sxs-lookup"><span data-stu-id="de8b4-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="de8b4-132">Следующие элементы программирования составляют API для диспетчера синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de8b4-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="de8b4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="de8b4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de8b4-134">О службе уведомлений о системных событиях</span><span class="sxs-lookup"><span data-stu-id="de8b4-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
