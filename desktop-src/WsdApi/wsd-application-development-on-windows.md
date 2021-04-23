---
description: API веб-служб Майкрософт на устройствах (WSDAPI) поддерживает реализацию управляемых клиентом устройств и служб, а также узлы устройств, соответствующие профилю устройств для веб-служб (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Разработка приложений WSD в Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712029"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="fd77c-103">Разработка приложений WSD в Windows</span><span class="sxs-lookup"><span data-stu-id="fd77c-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="fd77c-104">API веб-служб Майкрософт на устройствах (WSDAPI) поддерживает реализацию управляемых клиентом устройств и служб, а также узлы устройств, соответствующие [профилю устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="fd77c-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="fd77c-105">WSDAPI может использоваться для разработки как клиентских, так и серверных реализаций (устройств).</span><span class="sxs-lookup"><span data-stu-id="fd77c-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="fd77c-106">Очень часто код WSDAPI для этих приложений создается с помощью [всдкодежен](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="fd77c-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="fd77c-107">Некоторые функции и методы WSDAPI предназначены для вызова только в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="fd77c-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="fd77c-108">Справочная документация по API указывает, когда следует использовать или реализовывать функцию или метод только в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="fd77c-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="fd77c-109">В Windows SDK содержатся примеры WSDL-файлов, файлы конфигурации Всдкодежен и созданный код.</span><span class="sxs-lookup"><span data-stu-id="fd77c-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="fd77c-110">Дополнительные сведения см. в разделе [примеры WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="fd77c-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="fd77c-111">Если требуется перечислить устройства с помощью протокола WSD и запросить метаданные устройства WSD, можно использовать API [обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal) .</span><span class="sxs-lookup"><span data-stu-id="fd77c-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="fd77c-112">Если вы хотите реализовать WSD-устройство, которое не работает под управлением Windows, см. раздел [Разработка устройств WSD](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="fd77c-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
