---
description: Корпорация Майкрософт реализовала массив расширений для формата файла автоматической настройки Navigator, чтобы добавить поддержку IPv6 в вспомогательные функции WinINet и WinHTTP WPAD.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Расширения IPv6 для формата файла автоматической настройки Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684216"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="ce033-103">Расширения IPv6 для формата файла автоматической настройки Navigator</span><span class="sxs-lookup"><span data-stu-id="ce033-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="ce033-104">Корпорация Майкрософт реализовала массив расширений для формата файла автоматической настройки Navigator, чтобы добавить поддержку IPv6 в вспомогательные функции WinINet и WinHTTP WPAD.</span><span class="sxs-lookup"><span data-stu-id="ce033-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="ce033-105">Развертывание Интернета в конце 1990 г. привело к неожиданному нехваткеу IPv4-адресов, при этом пул будет исчерпан ежедневно.</span><span class="sxs-lookup"><span data-stu-id="ce033-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="ce033-106">IPv6 предоставляет решение этой проблемы, хотя в настоящее время она не развернута, ее использование, в определенном случае, станет более распространенным в будущем.</span><span class="sxs-lookup"><span data-stu-id="ce033-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="ce033-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) — это протокол, позволяющий веб-клиентам автоматически обнаруживать правильную конфигурацию прокси для исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="ce033-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="ce033-108">Это очень полезно для корпоративных развертываний, поскольку позволяет ИТ-администраторам настраивать сложные сценарии, которые могут маршрутизировать трафик для всех клиентов на определенные прокси-серверы на основе целевого сервера, к которому клиенты пытаются подключиться.</span><span class="sxs-lookup"><span data-stu-id="ce033-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="ce033-109">Службы WinINet и WinHTTP поддерживают вспомогательные функции WPAD в соответствии со [спецификацией формата файла настройки прокси-сервера Navigator (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), который стал стандартом де-факто.</span><span class="sxs-lookup"><span data-stu-id="ce033-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="ce033-110">К сожалению, эта спецификация была написана на 1996 и не определяет, что должно делать поведение функции при развертывании скрипта WPAD в сети с поддержкой IPv6.</span><span class="sxs-lookup"><span data-stu-id="ce033-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="ce033-111">Так как IPv6 является волной в будущем, все компоненты Windows теперь поддерживают два стека (IPv4 и IPv6) и только IPv6-сети.</span><span class="sxs-lookup"><span data-stu-id="ce033-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="ce033-112">Для поддержки IPv6 без влияния на существующее развертывание Корпорация Майкрософт добавила 6 новых функций вспомогательного класса в качестве расширения в спецификацию формата файла-посредника Navigator (PAC), а также добавил новую функцию с поддержкой IPv6, именуемую **финдпроксифорурлекс** , которую администраторы могут реализовать в скрипте WPAD.</span><span class="sxs-lookup"><span data-stu-id="ce033-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="ce033-113">Определения API вспомогательных функций прокси-сервера с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="ce033-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="ce033-114">Различия между вспомогательными функциями IPv6-Aware WPAD и устаревшими вспомогательными функциями WPAD</span><span class="sxs-lookup"><span data-stu-id="ce033-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="ce033-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ce033-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="ce033-116">Для этой функции требуется Windows Internet Explorer 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ce033-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



