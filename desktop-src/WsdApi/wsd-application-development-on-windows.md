---
description: Узнайте, как использовать API веб-служб Майкрософт на устройствах (WSD) для реализации устройств и служб, управляемых клиентом, а также для узлов устройств, которые соответствует DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Разработка приложений WSD в Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405787"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="a81f5-103">Разработка приложений WSD в Windows</span><span class="sxs-lookup"><span data-stu-id="a81f5-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="a81f5-104">API веб-служб Майкрософт на устройствах (WSDAPI) поддерживает реализацию управляемых клиентом устройств и служб, а также узлы устройств, соответствующие [профилю устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="a81f5-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="a81f5-105">WSDAPI может использоваться для разработки как клиентских, так и серверных реализаций (устройств).</span><span class="sxs-lookup"><span data-stu-id="a81f5-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="a81f5-106">Очень часто код WSDAPI для этих приложений создается с помощью [всдкодежен](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="a81f5-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="a81f5-107">Некоторые функции и методы WSDAPI предназначены для вызова только в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="a81f5-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="a81f5-108">Справочная документация по API указывает, когда следует использовать или реализовывать функцию или метод только в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="a81f5-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="a81f5-109">В Windows SDK содержатся примеры WSDL-файлов, файлы конфигурации Всдкодежен и созданный код.</span><span class="sxs-lookup"><span data-stu-id="a81f5-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="a81f5-110">Дополнительные сведения см. в разделе [примеры WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a81f5-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="a81f5-111">Если требуется перечислить устройства с помощью протокола WSD и запросить метаданные устройства WSD, можно использовать API [обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal) .</span><span class="sxs-lookup"><span data-stu-id="a81f5-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="a81f5-112">Если вы хотите реализовать WSD-устройство, которое не работает под управлением Windows, см. раздел [Разработка устройств WSD](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="a81f5-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
