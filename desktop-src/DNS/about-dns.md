---
title: Сведения о DNS
description: Служба доменных имен (DNS) является стандартным промышленным протоколом, используемым для нахождение компьютеров в сети на основе IP-адресов. Пользователи могут запоминать отображаемые имена, такие как www.microsoft.com, проще, чем адреса на основе чисел, например 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Сведения об DNS системы доменных имен
- DNS системы доменных имен, сведения
- DNS-сервер системы доменных имен, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104273670"
---
# <a name="about-dns"></a><span data-ttu-id="e766f-107">Сведения о DNS</span><span class="sxs-lookup"><span data-stu-id="e766f-107">About DNS</span></span>

<span data-ttu-id="e766f-108">Служба доменных имен (DNS) является стандартным промышленным протоколом, используемым для нахождение компьютеров в сети на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e766f-108">Domain Name System (DNS) is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="e766f-109">Пользователи могут запоминать отображаемые имена, например, так же, как `www.microsoft.com` адреса на основе чисел, например 207.46.131.137.</span><span class="sxs-lookup"><span data-stu-id="e766f-109">Users can remember display names, such as `www.microsoft.com` easier than number-based addresses, such as 207.46.131.137.</span></span>

<span data-ttu-id="e766f-110">IP-сети, такие как сети Интернет и Windows, используют адреса на основе чисел для передачи данных по сети. Поэтому необходимо преобразовать отображаемые имена (например, `www.microsoft.com` ) в числовые адреса, которые может распознать сеть (например, 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="e766f-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to transmit data throughout the network; therefore, it is necessary to translate display names (such as `www.microsoft.com`) into numeric addresses that the network can recognize (such as 207.46.131.137).</span></span> <span data-ttu-id="e766f-111">DNS — это служба, выбранная в Windows для размещения таких ресурсов и перевода их в IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e766f-111">DNS is the service of choice in Windows to locate such resources and translate them into IP addresses.</span></span>

<span data-ttu-id="e766f-112">DNS является основной службой локатора для Active Directory, поэтому DNS может рассматриваться как базовая служба для Windows и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e766f-112">DNS is the primary locator service for Active Directory, and therefore, DNS can be considered a base service for both Windows and Active Directory.</span></span> <span data-ttu-id="e766f-113">Windows предоставляет функции, позволяющие программистам приложений использовать функции DNS, такие как программное выполнение запросов DNS, Сравнение записей и поиск имен.</span><span class="sxs-lookup"><span data-stu-id="e766f-113">Windows provides functions that enable application programmers to use DNS functions such as programmatically making DNS queries, comparing records, and looking up names.</span></span>

<span data-ttu-id="e766f-114">Многие функции DNS фактически являются типами функций, в которых существует базовое имя для функции, но ее использование зависит от кодировки символов.</span><span class="sxs-lookup"><span data-stu-id="e766f-114">Many DNS functions are actually function types, in that there is a base name for the function, but its use depends on character encoding.</span></span> <span data-ttu-id="e766f-115">Например, функция [**днскуери**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) указана в справочнике по функциям интерфейса прикладного программирования (API) DNS как **днскуери**. но его использование в приложениях зависит от того, является ли кодировка символов ANSI (обозначена присоединением \_ к имени типа функции), Юникод (обозначено добавлением \_ W к имени типа функции) или UTF-8 (задается путем добавления \_ UTF к имени типа функции).</span><span class="sxs-lookup"><span data-stu-id="e766f-115">For example, the [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) function is listed in the function reference of the DNS Application Programming Interface (API) as **DnsQuery**, but its use in applications depends on whether the character encoding is ANSI (designated by appending \_A to the function type name), Unicode (designated by appending \_W to the function type name), or UTF-8 (designated by appending \_UTF to the function type name).</span></span> <span data-ttu-id="e766f-116">Поэтому вызов функции для функции **днскуери** на самом деле будет одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="e766f-116">Therefore, the function call for the **DnsQuery** function would actually be one of the following:</span></span>

<span data-ttu-id="e766f-117">Днскуери \_ a ( \_ для кодирования ANSI)</span><span class="sxs-lookup"><span data-stu-id="e766f-117">DnsQuery\_A (\_A for ANSI encoding)</span></span>

<span data-ttu-id="e766f-118">Днскуери \_ w ( \_ w для кодирования в Юникоде)</span><span class="sxs-lookup"><span data-stu-id="e766f-118">DnsQuery\_W (\_W for Unicode encoding)</span></span>

<span data-ttu-id="e766f-119">Днскуери \_ UTF8 ( \_ UTF8 для кодировки UTF-8)</span><span class="sxs-lookup"><span data-stu-id="e766f-119">DnsQuery\_UTF8 (\_UTF8 for UTF-8 encoding)</span></span>

<span data-ttu-id="e766f-120">Все функции, которым требуется это соглашение, четко занимают это требование в первых нескольких предложениях своего определения функции.</span><span class="sxs-lookup"><span data-stu-id="e766f-120">All functions that require this convention clearly state this requirement within the first few sentences of their function definition.</span></span> <span data-ttu-id="e766f-121">Используйте правильное имя функции; Например, нельзя просто вызвать [**днскуери**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) вместо днскуери \_ .</span><span class="sxs-lookup"><span data-stu-id="e766f-121">Use the proper function name; for example, you cannot simply call [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) instead of DnsQuery\_A.</span></span>

 

 




