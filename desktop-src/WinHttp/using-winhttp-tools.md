---
description: Сведения о командах, которые можно использовать в Windows Vista и более поздних версиях для настройки параметров прокси-сервера и трассировки для HTTP-протокола Windows, см. в разделе Netsh Commands for Windows гипертекста Protocol (WINHTTP).
ms.assetid: 81f6b25e-ea14-4dbd-a715-926db7cf90e7
title: Использование средств WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e402962dc34cbf654fa8db49f96b86e7406a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711072"
---
# <a name="using-winhttp-tools"></a><span data-ttu-id="c392b-103">Использование средств WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c392b-103">Using WinHTTP Tools</span></span>

<span data-ttu-id="c392b-104">Сведения о командах, которые можно использовать в Windows Vista и более поздних версиях для настройки параметров прокси-сервера и трассировки для HTTP-протокола Windows, см. в разделе [netsh Commands for Windows гипертекста Protocol (WinHTTP)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="c392b-104">For the commands you can use in Windows Vista and later to configure proxy and tracing settings for Windows HTTP , see [Netsh Commands for Windows Hypertext Transfer Protocol (WINHTTP)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)).</span></span>

<span data-ttu-id="c392b-105">**Windows Server 2003 и более ранние версии:** Существует несколько средств, которые могут помочь в написании и отладке приложений.</span><span class="sxs-lookup"><span data-stu-id="c392b-105">**Windows Server 2003 and Earlier:** There are several tools that are available to help you write and debug your applications.</span></span> <span data-ttu-id="c392b-106">Они описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c392b-106">They are explained in the following topics:</span></span>

-   <span data-ttu-id="c392b-107">[WinHttpCfg.exe, средство настройки сертификатов](winhttpcertcfg-exe--a-certificate-configuration-tool.md) позволяет администраторам устанавливать и настраивать сертификаты клиентов в любом [*хранилище сертификатов*](glossary.md) , доступ к которому может получить учетная запись диспетчера веб-приложений (IWAM) Internet Server.</span><span class="sxs-lookup"><span data-stu-id="c392b-107">[WinHttpCfg.exe, a Certificate Configuration Tool](winhttpcertcfg-exe--a-certificate-configuration-tool.md) enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="c392b-108">Это средство также устраняет необходимость в специальных возможностях для учетных записей, таких как учетная запись IWAM, для получения доступа к сертификатам при использовании Active Server страниц (ASP).</span><span class="sxs-lookup"><span data-stu-id="c392b-108">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>
-   <span data-ttu-id="c392b-109">[Netsh.exe или ProxyCfg.exe прокси средства настройки](proxycfg-exe--a-proxy-configuration-tool.md) можно использовать для настройки прокси-серверов с помощью служб Microsoft Windows HTTP (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="c392b-109">[Netsh.exe or ProxyCfg.exe Proxy Configuration Tools](proxycfg-exe--a-proxy-configuration-tool.md) can be used to configure proxy servers with Microsoft Windows HTTP Services (WinHTTP).</span></span>
-   <span data-ttu-id="c392b-110">[Винхттптрацекфг, средство настройки трассировки](winhttptracecfg-exe--a-trace-configuration-tool.md) предоставляет возможность отслеживать функции WinHTTP и соответствующий сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="c392b-110">[WinHttpTraceCfg, a Trace Configuration Tool](winhttptracecfg-exe--a-trace-configuration-tool.md) provides the ability to monitor WinHTTP functions and the corresponding network traffic.</span></span> <span data-ttu-id="c392b-111">Отладка приложений, использующих зашифрованные протоколы передачи данных, такие как SSL (SSL), исключает перехват пакетов на транспортном уровне сети и требует возможность перехвата трафика между клиентом и сервером после его расшифровки.</span><span class="sxs-lookup"><span data-stu-id="c392b-111">Debugging applications which utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="c392b-112">Средство трассировки WinHTTP имеет ряд возможностей для перехвата потока трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="c392b-112">The WinHTTP trace facility has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

 

 
