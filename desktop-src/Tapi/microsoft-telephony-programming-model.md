---
description: Модель программирования Microsoft для телефонии абстрагирует Управление связью с помощью управления устройствами, освобождая приложения конечных пользователей и производителей устройств от необходимости марта в локкстеп.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Модель программирования телефонии Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682384"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="13326-103">Модель программирования телефонии Microsoft</span><span class="sxs-lookup"><span data-stu-id="13326-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="13326-104">Модель программирования Microsoft для телефонии абстрагирует Управление связью с помощью управления устройствами, освобождая приложения конечных пользователей и производителей устройств от необходимости марта в локкстеп.</span><span class="sxs-lookup"><span data-stu-id="13326-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="13326-105">При использовании этой модели для конечного пользователя или серверного приложения не требуется подробная информация об управлении устройством, и устройство не обязательно должно быть адаптировано для приложения.</span><span class="sxs-lookup"><span data-stu-id="13326-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="13326-106">Приложения и устройства могут выполнять инновации и изменять их без каких бы то ни было бесполезными для клиентов.</span><span class="sxs-lookup"><span data-stu-id="13326-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="13326-107">На следующей схеме показано, как выполняется эта абстракция.</span><span class="sxs-lookup"><span data-stu-id="13326-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![как TAPI абстрагирует управление взаимодействием с контролем устройств](images/tapicomp.png)

<span data-ttu-id="13326-109">Эти компоненты можно просмотреть в виде репозиториев специализированных знаний.</span><span class="sxs-lookup"><span data-stu-id="13326-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="13326-110">Приложение интерфейса программирования приложений телефонии (TAPI) знает потребности пользователей, библиотеку DLL TAPI и ТАПИСРВ общие телефонные соединения, а поставщики услуг (TSP и MSP) знают о подробном контроле устройств.</span><span class="sxs-lookup"><span data-stu-id="13326-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="13326-111">Средствам записи приложений и производителям устройств требуются только общие сведения о требованиях друг друга.</span><span class="sxs-lookup"><span data-stu-id="13326-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="13326-112">Приложение загружает библиотеку DLL TAPI в пространство процесса и использует TAPI для обмена данными с потребностями.</span><span class="sxs-lookup"><span data-stu-id="13326-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="13326-113">TAPI устанавливает связь RPC с сервером TAPI.</span><span class="sxs-lookup"><span data-stu-id="13326-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="13326-114">Кроме того, TAPI 3. x создает объект MSP и обменивается данными с ним с помощью определенного набора команд, интерфейса поставщика услуг мультимедиа (МСПИ).</span><span class="sxs-lookup"><span data-stu-id="13326-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="13326-115">Когда приложение вызывает операцию TAPI, Библиотека динамической компоновки TAPI проверяет и маршалирует параметры, а затем пересылает сведения в ТАПИСРВ.</span><span class="sxs-lookup"><span data-stu-id="13326-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="13326-116">ТАПИСРВ отслеживает коммуникационные ресурсы, доступные локальному компьютеру, и интерфейсы с поставщиками услуг телефонии (специалистами) с помощью интерфейса поставщика услуг телефонии (ТСПИ).</span><span class="sxs-lookup"><span data-stu-id="13326-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="13326-117">Обмен данными между TSP и MSP выполняется с помощью виртуального подключения, которое проходит через библиотеку DLL и ТАПИСРВ.</span><span class="sxs-lookup"><span data-stu-id="13326-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="13326-118">Пара TSP/MSP предоставляет сведения о состоянии и возможностях устройства и реализует конкретные команды, необходимые для требуемого ответа.</span><span class="sxs-lookup"><span data-stu-id="13326-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="13326-119">Результатом использования этой модели программирования является то, что приложения могут пропускать или корректировать изменения на устройствах, а новые устройства могут быть сразу же полезны вместо того, чтобы ожидать изменения в базовом коде.</span><span class="sxs-lookup"><span data-stu-id="13326-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="13326-120">Потенциальная доля рынка расширяется как для модулей записи приложений, так и для производителей устройств.</span><span class="sxs-lookup"><span data-stu-id="13326-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="13326-121">В следующих разделах более подробно описаны компоненты телефонии Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="13326-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="13326-122">Приложения TAPI</span><span class="sxs-lookup"><span data-stu-id="13326-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="13326-123">БИБЛИОТЕКА DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="13326-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="13326-124">Сервер TAPI</span><span class="sxs-lookup"><span data-stu-id="13326-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="13326-125">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="13326-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="13326-126">Синхронная или асинхронная модель</span><span class="sxs-lookup"><span data-stu-id="13326-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="13326-127">Структуры данных TAPI</span><span class="sxs-lookup"><span data-stu-id="13326-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="13326-128">Уровни обслуживания TAPI</span><span class="sxs-lookup"><span data-stu-id="13326-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 



