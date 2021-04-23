---
description: Важно убедиться, что новые приложения Winsock и существующие приложения полностью совместимы с IPv6.
ms.assetid: 48aa6be8-e8a2-48a5-aa71-3e5ed7032551
title: IP версии 6 (IPv6)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9647b70571b0bc81cbea508cf2e3bb55662efdf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897333"
---
# <a name="internet-protocol-version-6-ipv6"></a><span data-ttu-id="b6175-103">IP версии 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b6175-103">Internet Protocol Version 6 (IPv6)</span></span>

<span data-ttu-id="b6175-104">Важно убедиться, что новые приложения Winsock и существующие приложения полностью совместимы с IPv6.</span><span class="sxs-lookup"><span data-stu-id="b6175-104">It is important to ensure that new Winsock applications as well as existing applications are fully compatible with IPv6.</span></span> <span data-ttu-id="b6175-105">Доступность пространства адресов IPv4 для новых выделений IPv4-адресов была исчерпана для Азии и Тихоокеанского региона в 2011.</span><span class="sxs-lookup"><span data-stu-id="b6175-105">The availability of the IPv4 address space for new IPv4 address allocations was exhausted for Asia and the Pacific in 2011.</span></span> <span data-ttu-id="b6175-106">В течение нескольких лет ожидается, что другие части мира будут исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="b6175-106">Other parts of the world are expected to be exhausted in a few years.</span></span>

<span data-ttu-id="b6175-107">По адресу IPv6 доступны новые веб-сайты и службы с растущим процентом.</span><span class="sxs-lookup"><span data-stu-id="b6175-107">A growing percentage of new websites and services are available using IPv6 addresses.</span></span> <span data-ttu-id="b6175-108">Многие пользователи Интернета на новых рынках зависят от IPv6 для доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="b6175-108">Many Internet users in emerging markets are dependent on IPv6 for Internet access.</span></span>

<span data-ttu-id="b6175-109">Корпорация Майкрософт обладает долгим обязательством по поддержке IPv6.</span><span class="sxs-lookup"><span data-stu-id="b6175-109">Microsoft has a long commitment of supporting IPv6.</span></span> <span data-ttu-id="b6175-110">Полная поддержка IPv6 предоставляется в Windows XP с пакетом обновления 1 (SP1) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b6175-110">Full IPv6 support is provided on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="b6175-111">В этом документе содержатся сведения о поддержке Winsock для IPv6:</span><span class="sxs-lookup"><span data-stu-id="b6175-111">This document provides information about the Winsock support for IPv6:</span></span>

-   [<span data-ttu-id="b6175-112">Использование IPv6</span><span class="sxs-lookup"><span data-stu-id="b6175-112">Using IPv6</span></span>](using-ipv6-2.md)
-   [<span data-ttu-id="b6175-113">Использование Internet Explorer для доступа к веб-сайтам IPv6</span><span class="sxs-lookup"><span data-stu-id="b6175-113">Using Internet Explorer to Access IPv6 Websites</span></span>](using-internet-explorer-to-access-ipv6-web-sites-2.md)
-   [<span data-ttu-id="b6175-114">Рекомендуемые конфигурации для IPv6</span><span class="sxs-lookup"><span data-stu-id="b6175-114">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
-   [<span data-ttu-id="b6175-115">Дополнительные разделы по IPv6</span><span class="sxs-lookup"><span data-stu-id="b6175-115">Additional IPv6 Topics</span></span>](additional-topics-2.md)

<span data-ttu-id="b6175-116">Дополнительные сведения о добавлении возможностей IPv6 в приложения Windows Sockets см. в разделе [рекомендации по IPv6 для приложений Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="b6175-116">For additional information on adding IPv6 capability to your Windows Sockets applications, see [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

<span data-ttu-id="b6175-117">Общие сведения о протоколе IPv6, а также обзорные технологии развертывания и туннелирования IPv6 доступны в TechNet по [протоколу Microsoft Internet Protocol версии 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b6175-117">An introduction to the IPv6 protocol along with overviews on deployment and IPv6 transitioning technologies is available on Technet at [Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6175-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b6175-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6175-119">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b6175-119">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="b6175-120">Поддержка IPv6</span><span class="sxs-lookup"><span data-stu-id="b6175-120">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="b6175-121">Предварительный просмотр технологии IPv6 для Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6175-121">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

<span data-ttu-id="b6175-122">[Протокол Microsoft IP версии 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b6175-122">[Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span></span>
</dt> </dl>

 

 
