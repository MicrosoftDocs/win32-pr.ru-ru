---
description: Приложения, использующие направленное обнаружение, отправляют сообщения проверки по протоколу HTTP или HTTPS для обнаружения устройств.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Устранение неполадок приложений WSDAPI с использованием направленного обнаружения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544791"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="5002a-103">Устранение неполадок приложений WSDAPI с использованием направленного обнаружения</span><span class="sxs-lookup"><span data-stu-id="5002a-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="5002a-104">Приложения, использующие направленное обнаружение, отправляют сообщения [проверки](probe-message.md) по протоколу HTTP или HTTPS для обнаружения устройств.</span><span class="sxs-lookup"><span data-stu-id="5002a-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="5002a-105">Соответствующие сообщения [ProbeMatch](probematches-message.md) , отправленные в ответе, также передаются по протоколу HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5002a-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="5002a-106">Направленное обнаружение может инициироваться мастером добавления принтера, клиентом обнаружения функций или приложением WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="5002a-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="5002a-107">Сообщения зонда и ProbeMatch структурно идентичны переданным по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="5002a-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="5002a-108">Сообщения добавляются с соответствующими заголовками HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5002a-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="5002a-109">Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением с помощью направленного обнаружения.</span><span class="sxs-lookup"><span data-stu-id="5002a-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="5002a-110">**Устранение неполадок приложения WSDAPI с помощью направленного обнаружения**</span><span class="sxs-lookup"><span data-stu-id="5002a-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="5002a-111">[Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5002a-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="5002a-112">[Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="5002a-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="5002a-113">[Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="5002a-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="5002a-114">[Проверка трассировки сети для приложения с помощью направленного обнаружения](inspecting-network-traces-for-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="5002a-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="5002a-115">Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5002a-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5002a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5002a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5002a-117">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="5002a-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="5002a-118">Устранение неполадок мастера добавления принтера</span><span class="sxs-lookup"><span data-stu-id="5002a-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="5002a-119">Устранение неполадок приложений WSDAPI</span><span class="sxs-lookup"><span data-stu-id="5002a-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



