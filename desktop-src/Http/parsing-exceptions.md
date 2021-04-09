---
title: Синтаксический анализ исключений
description: API сервера HTTP предоставляет разделы реестра для поддержки анализа исключений в спецификации HTTP/1.1 для обратной совместимости.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Синтаксический анализ исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986584"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="15d57-104">Синтаксический анализ исключений</span><span class="sxs-lookup"><span data-stu-id="15d57-104">Parsing Exceptions</span></span>

<span data-ttu-id="15d57-105">API сервера HTTP предоставляет разделы реестра для поддержки анализа исключений в спецификации HTTP/1.1 для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="15d57-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="15d57-106">Эти исключения не включены по умолчанию и должны быть включены только для каждого случая, когда сервер испытывает проблемы совместимости с клиентами HTTP.</span><span class="sxs-lookup"><span data-stu-id="15d57-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="15d57-107">Эти значения создаются в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="15d57-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="15d57-108">В следующей таблице перечислены разделы реестра, предоставляемые для поддержки перечисленных исключений.</span><span class="sxs-lookup"><span data-stu-id="15d57-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="15d57-109">Чтобы включить исключение, установите соответствующее значение ключа равным 1 и перезапустите службу HTTP.</span><span class="sxs-lookup"><span data-stu-id="15d57-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="15d57-110">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="15d57-110">Key name</span></span>                              | <span data-ttu-id="15d57-111">Описание</span><span class="sxs-lookup"><span data-stu-id="15d57-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d57-112">Алловвеакхеадернамесинтакс (DWORD)</span><span class="sxs-lookup"><span data-stu-id="15d57-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="15d57-113">Позволяет анализатору HTTP принимать имена заголовков с символами-разделителями, такими как "?".</span><span class="sxs-lookup"><span data-stu-id="15d57-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="15d57-114">Алловвеакхеадервалуесинтакс (DWORD)</span><span class="sxs-lookup"><span data-stu-id="15d57-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="15d57-115">Позволяет средству синтаксического анализа HTTP принимать значения заголовка с необработанными управляющими символами (без экранирования).</span><span class="sxs-lookup"><span data-stu-id="15d57-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="15d57-116">Алловкасеинсенситивевербс (DWORD)</span><span class="sxs-lookup"><span data-stu-id="15d57-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="15d57-117">Позволяет средству синтаксического анализа HTTP принимать строчные методы HTTP и глаголы, такие как Get.</span><span class="sxs-lookup"><span data-stu-id="15d57-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="15d57-118">Алловунескапедрестриктедчарс (DWORD)</span><span class="sxs-lookup"><span data-stu-id="15d57-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="15d57-119">Позволяет анализатору HTTP принимать управляющие символы в абспас и строки запросов URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="15d57-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="15d57-120">В случае использования абсолютного URL-адреса управляющие символы не будут разрешены в имени узла.</span><span class="sxs-lookup"><span data-stu-id="15d57-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="15d57-121">Все разновидности URL-адресов, а именно UTF8, DBCS и ANSI, позволят использовать управляющие символы.</span><span class="sxs-lookup"><span data-stu-id="15d57-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="15d57-122">Все управляющие символы ASCII, кроме NUL (0x00), LF (0x0A), CR (0x0D) и Horizontal Tab (0x09), будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="15d57-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




