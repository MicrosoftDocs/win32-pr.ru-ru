---
title: Интерфейсы API UPnP
description: Инфраструктура UPnP обеспечивает динамическую сеть интеллектуальных устройств, беспроводных устройств и компьютеров.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104134738"
---
# <a name="upnp-apis"></a><span data-ttu-id="c7978-104">Интерфейсы API UPnP</span><span class="sxs-lookup"><span data-stu-id="c7978-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="c7978-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="c7978-105">Purpose</span></span>

<span data-ttu-id="c7978-106">Инфраструктура UPnP обеспечивает динамическую сеть интеллектуальных устройств, беспроводных устройств и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c7978-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="c7978-107">Для работы с устройствами, сертифицированными для UPnP, предусмотрены два API-интерфейса:</span><span class="sxs-lookup"><span data-stu-id="c7978-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="c7978-108">API контрольной точки, состоящий из набора COM-интерфейсов, используемых для поиска и управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="c7978-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="c7978-109">API узла устройства, который состоит из набора COM-интерфейсов, используемых для реализации устройств, размещенных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c7978-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c7978-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="c7978-110">Where applicable</span></span>

<span data-ttu-id="c7978-111">API контрольной точки позволяет разработчикам создавать приложения, которые выполняют поиск и управление устройствами, сертифицированными для UPnP.</span><span class="sxs-lookup"><span data-stu-id="c7978-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="c7978-112">API узла устройства позволяет разработчикам реализовать функциональность устройств, сертифицированных с помощью UPnP, и использовать узел устройства для управления функциями обнаружения, описания, управления, представлениями и событиями устройства, сертифицированными для UPnP.</span><span class="sxs-lookup"><span data-stu-id="c7978-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c7978-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c7978-113">Developer audience</span></span>

<span data-ttu-id="c7978-114">Разработчики, использующие API-интерфейсы контрольных точек и API узла устройств, должны быть знакомы с архитектурой UPnP-устройств.</span><span class="sxs-lookup"><span data-stu-id="c7978-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="c7978-115">Дополнительные сведения см. в [документации по реализации UPnP](https://openconnectivity.org/resources/upnpresources.zip) и на [форуме UPnP](https://openconnectivity.org/).</span><span class="sxs-lookup"><span data-stu-id="c7978-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="c7978-116">Разработчики, использующие API узла устройства, должны быть знакомы с интерфейсами ATL и COM.</span><span class="sxs-lookup"><span data-stu-id="c7978-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="c7978-117">API контрольных точек и API-интерфейсы узла устройств используются различными приложениями, из сценариев, внедренных в HTML-страницы, в полноценные программы C++ и Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c7978-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="c7978-118">Только API контрольной точки поддерживает Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c7978-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c7978-119">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c7978-119">Run-time requirements</span></span>

<span data-ttu-id="c7978-120">API контрольной точки используется на компьютерах под управлением Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional и Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="c7978-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="c7978-121">API узла устройства используется на компьютерах под управлением Windows XP, Windows XP Professional и Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="c7978-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="c7978-122">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделе "требования" в документации.</span><span class="sxs-lookup"><span data-stu-id="c7978-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c7978-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c7978-123">In this section</span></span>



| <span data-ttu-id="c7978-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="c7978-124">Topic</span></span>                                                                                          | <span data-ttu-id="c7978-125">Описание</span><span class="sxs-lookup"><span data-stu-id="c7978-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7978-126">Общие сведения об архитектуре UPnP</span><span class="sxs-lookup"><span data-stu-id="c7978-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="c7978-127">Общие сведения и фон.</span><span class="sxs-lookup"><span data-stu-id="c7978-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="c7978-128">Общие сведения о точке управления</span><span class="sxs-lookup"><span data-stu-id="c7978-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="c7978-129">Общие сведения об API контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="c7978-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="c7978-130">Использование API контрольной точки</span><span class="sxs-lookup"><span data-stu-id="c7978-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="c7978-131">Пример кода, демонстрирующий разработку приложений, контролирующих устройства, сертифицированные для UPnP.</span><span class="sxs-lookup"><span data-stu-id="c7978-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="c7978-132">Справочник по API контрольной точки</span><span class="sxs-lookup"><span data-stu-id="c7978-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="c7978-133">Документация по интерфейсам, методам и событиям компонентов контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="c7978-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="c7978-134">Общие сведения об API узла устройства</span><span class="sxs-lookup"><span data-stu-id="c7978-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="c7978-135">Общие сведения об API узла устройства.</span><span class="sxs-lookup"><span data-stu-id="c7978-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="c7978-136">Использование API узла устройства</span><span class="sxs-lookup"><span data-stu-id="c7978-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="c7978-137">Пример кода, демонстрирующий разработку приложения для устройств, сертифицированных для UPnP.</span><span class="sxs-lookup"><span data-stu-id="c7978-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="c7978-138">Справочник по API узла устройства</span><span class="sxs-lookup"><span data-stu-id="c7978-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="c7978-139">Документация по интерфейсам, методам и событиям компонентов узла устройств.</span><span class="sxs-lookup"><span data-stu-id="c7978-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





