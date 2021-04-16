---
description: API веб-служб Майкрософт на устройствах (WSDAPI) поддерживает реализацию управляемых клиентом устройств и служб, а также узлы устройств, соответствующие профилю устройств для веб-служб (DPWS).
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Веб-службы на устройствах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692684"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="75132-103">Веб-службы на устройствах</span><span class="sxs-lookup"><span data-stu-id="75132-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="75132-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="75132-104">Purpose</span></span>

<span data-ttu-id="75132-105">API веб-служб Майкрософт на устройствах (WSDAPI) поддерживает реализацию управляемых клиентом устройств и служб, а также узлы устройств, соответствующие [профилю устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="75132-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="75132-106">WSDAPI использует [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) для обнаружения устройств.</span><span class="sxs-lookup"><span data-stu-id="75132-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="75132-107">WSDAPI может использоваться для разработки обеих реализаций клиента и службы.</span><span class="sxs-lookup"><span data-stu-id="75132-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="75132-108">Где применимо</span><span class="sxs-lookup"><span data-stu-id="75132-108">Where applicable</span></span>

<span data-ttu-id="75132-109">Веб-службы на устройствах позволяют клиенту обнаруживать и получать доступ к удаленному устройству и связанным с ним службам по сети.</span><span class="sxs-lookup"><span data-stu-id="75132-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="75132-110">Он поддерживает обнаружение устройств, описание, управление и события.</span><span class="sxs-lookup"><span data-stu-id="75132-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="75132-111">Разработчики могут создавать прокси-серверы клиента WSDAPI и соответствующие заглушки для узлов устройств.</span><span class="sxs-lookup"><span data-stu-id="75132-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="75132-112">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="75132-112">Developer audience</span></span>

<span data-ttu-id="75132-113">Документация по веб-службам на устройствах предназначена для программистов C/C++ и поставщиков устройств, создающих продукты, соответствующие DPWS.</span><span class="sxs-lookup"><span data-stu-id="75132-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="75132-114">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="75132-114">Run-time requirements</span></span>

<span data-ttu-id="75132-115">Клиентские приложения, использующие WSDAPI, поддерживаются начиная с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="75132-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75132-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="75132-116">In this section</span></span>



| <span data-ttu-id="75132-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="75132-117">Topic</span></span>                                                                                  | <span data-ttu-id="75132-118">Описание</span><span class="sxs-lookup"><span data-stu-id="75132-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75132-119">О веб-службах на устройствах</span><span class="sxs-lookup"><span data-stu-id="75132-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="75132-120">Архитектура и общие сведения о веб-службах на устройствах.</span><span class="sxs-lookup"><span data-stu-id="75132-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="75132-121">Использование веб-служб на устройствах</span><span class="sxs-lookup"><span data-stu-id="75132-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="75132-122">Сведения о создании кода, настройке приложений и устранении неполадок.</span><span class="sxs-lookup"><span data-stu-id="75132-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="75132-123">Справочник по веб-службам на устройствах</span><span class="sxs-lookup"><span data-stu-id="75132-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="75132-124">Справочная документация по API веб-служб на устройствах.</span><span class="sxs-lookup"><span data-stu-id="75132-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="75132-125">См. также</span><span class="sxs-lookup"><span data-stu-id="75132-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75132-126">Блог "Дрисколл"</span><span class="sxs-lookup"><span data-stu-id="75132-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

