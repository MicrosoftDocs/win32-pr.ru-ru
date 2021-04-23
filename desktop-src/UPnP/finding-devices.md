---
title: Поиск устройств
description: Архитектура UPnP — это динамическая сетевая архитектура, которая позволяет устройствам присоединяться к сети и выходить из нее в любое время.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068439"
---
# <a name="finding-devices"></a><span data-ttu-id="69f31-103">Поиск устройств</span><span class="sxs-lookup"><span data-stu-id="69f31-103">Finding Devices</span></span>

<span data-ttu-id="69f31-104">Архитектура UPnP — это динамическая сетевая архитектура, которая позволяет устройствам присоединяться к сети и выходить из нее в любое время.</span><span class="sxs-lookup"><span data-stu-id="69f31-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="69f31-105">Из-за этой динамической архитектуры приложения не могут полагаться на определенные устройства UPnP, чтобы быть доступными в любой конкретный момент времени.</span><span class="sxs-lookup"><span data-stu-id="69f31-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="69f31-106">По этой причине приложения (или контрольные точки) выполняют поиск в сети, чтобы найти устройства, наиболее точно соответствующие указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="69f31-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="69f31-107">Приложения также ожидают сообщения объявления устройства, указывающие, что новые устройства были добавлены в сеть.</span><span class="sxs-lookup"><span data-stu-id="69f31-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="69f31-108">Ниже приведены допустимые условия поиска для устройств, основанных на UPnP.</span><span class="sxs-lookup"><span data-stu-id="69f31-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="69f31-109">Тип устройства</span><span class="sxs-lookup"><span data-stu-id="69f31-109">Device type</span></span>
-   <span data-ttu-id="69f31-110">Service type (Тип службы)</span><span class="sxs-lookup"><span data-stu-id="69f31-110">Service type</span></span>
-   <span data-ttu-id="69f31-111">Уникальное имя устройства (УДН)</span><span class="sxs-lookup"><span data-stu-id="69f31-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="69f31-112">Все корневые устройства</span><span class="sxs-lookup"><span data-stu-id="69f31-112">All root devices</span></span>

<span data-ttu-id="69f31-113">Поиск типа устройства и типа службы обычно используется для поиска класса устройств с общими характеристиками.</span><span class="sxs-lookup"><span data-stu-id="69f31-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="69f31-114">Поиск УДН используется для поиска конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="69f31-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="69f31-115">Для поиска устройств приложение должно сначала создать объект Finder устройства.</span><span class="sxs-lookup"><span data-stu-id="69f31-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="69f31-116">Этот объект предоставляет интерфейс [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) . его методы выполняют описанные выше операции поиска.</span><span class="sxs-lookup"><span data-stu-id="69f31-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="69f31-117">В следующих разделах описывается процесс поиска устройств.</span><span class="sxs-lookup"><span data-stu-id="69f31-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="69f31-118">Создание устройства поиска устройств</span><span class="sxs-lookup"><span data-stu-id="69f31-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="69f31-119">Асинхронный поиск</span><span class="sxs-lookup"><span data-stu-id="69f31-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="69f31-120">Синхронный поиск</span><span class="sxs-lookup"><span data-stu-id="69f31-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="69f31-121">Коллекции устройств, возвращенные синхронным поиском</span><span class="sxs-lookup"><span data-stu-id="69f31-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 




