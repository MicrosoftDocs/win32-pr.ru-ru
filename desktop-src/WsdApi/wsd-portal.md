---
description: Узнайте, как реализовать веб-службы на устройствах (WSD). Изучите его назначение, где это применимо, аудитория разработчика и требования к времени выполнения.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Веб-службы на устройствах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405757"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="dec13-104">Веб-службы на устройствах</span><span class="sxs-lookup"><span data-stu-id="dec13-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="dec13-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="dec13-105">Purpose</span></span>

<span data-ttu-id="dec13-106">API веб-служб Майкрософт на устройствах (WSDAPI) поддерживает реализацию управляемых клиентом устройств и служб, а также узлы устройств, соответствующие [профилю устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="dec13-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="dec13-107">WSDAPI использует [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) для обнаружения устройств.</span><span class="sxs-lookup"><span data-stu-id="dec13-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="dec13-108">WSDAPI может использоваться для разработки обеих реализаций клиента и службы.</span><span class="sxs-lookup"><span data-stu-id="dec13-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="dec13-109">Где применимо</span><span class="sxs-lookup"><span data-stu-id="dec13-109">Where applicable</span></span>

<span data-ttu-id="dec13-110">Веб-службы на устройствах позволяют клиенту обнаруживать и получать доступ к удаленному устройству и связанным с ним службам по сети.</span><span class="sxs-lookup"><span data-stu-id="dec13-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="dec13-111">Он поддерживает обнаружение устройств, описание, управление и события.</span><span class="sxs-lookup"><span data-stu-id="dec13-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="dec13-112">Разработчики могут создавать прокси-серверы клиента WSDAPI и соответствующие заглушки для узлов устройств.</span><span class="sxs-lookup"><span data-stu-id="dec13-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dec13-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="dec13-113">Developer audience</span></span>

<span data-ttu-id="dec13-114">Документация по веб-службам на устройствах предназначена для программистов C/C++ и поставщиков устройств, создающих продукты, соответствующие DPWS.</span><span class="sxs-lookup"><span data-stu-id="dec13-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="dec13-115">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="dec13-115">Run-time requirements</span></span>

<span data-ttu-id="dec13-116">Клиентские приложения, использующие WSDAPI, поддерживаются начиная с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dec13-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dec13-117">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="dec13-117">In this section</span></span>



| <span data-ttu-id="dec13-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="dec13-118">Topic</span></span>                                                                                  | <span data-ttu-id="dec13-119">Описание</span><span class="sxs-lookup"><span data-stu-id="dec13-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dec13-120">О веб-службах на устройствах</span><span class="sxs-lookup"><span data-stu-id="dec13-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="dec13-121">Архитектура и общие сведения о веб-службах на устройствах.</span><span class="sxs-lookup"><span data-stu-id="dec13-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="dec13-122">Использование веб-служб на устройствах</span><span class="sxs-lookup"><span data-stu-id="dec13-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="dec13-123">Сведения о создании кода, настройке приложений и устранении неполадок.</span><span class="sxs-lookup"><span data-stu-id="dec13-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="dec13-124">Справочник по веб-службам на устройствах</span><span class="sxs-lookup"><span data-stu-id="dec13-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="dec13-125">Справочная документация по API веб-служб на устройствах.</span><span class="sxs-lookup"><span data-stu-id="dec13-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="dec13-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dec13-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec13-127">Блог "Дрисколл"</span><span class="sxs-lookup"><span data-stu-id="dec13-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

