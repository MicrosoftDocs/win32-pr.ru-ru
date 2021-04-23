---
description: Размер запроса на дайджест-доступ должен быть менее 2048 байт.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Содержимое запроса дайджеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143750"
---
# <a name="contents-of-a-digest-challenge"></a><span data-ttu-id="9ac5b-103">Содержимое запроса дайджеста</span><span class="sxs-lookup"><span data-stu-id="9ac5b-103">Contents of a Digest Challenge</span></span>

<span data-ttu-id="9ac5b-104">Размер запроса на дайджест-доступ должен быть менее 2048 байт.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-104">The size of a Digest Access challenge must be less than 2048 bytes.</span></span> <span data-ttu-id="9ac5b-105">В следующем примере показана задача, назначенная строке символов Сзчалленже.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-105">The following example shows a challenge assigned to the character string szChallenge.</span></span>


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> <span data-ttu-id="9ac5b-106">Строка запроса заключается в двойные кавычки и содержит внедренные двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-106">The challenge string is enclosed in double quotes and contains embedded double quotes.</span></span> <span data-ttu-id="9ac5b-107">Перед внедренными двойными кавычками следует использовать обратную косую черту ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="9ac5b-107">Embedded double quotes must be preceded (escaped) with a backslash (\\).</span></span>

 

<span data-ttu-id="9ac5b-108">Запрос дайджеста может содержать следующие директивы.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-108">A Digest challenge can contain the following directives.</span></span>



| <span data-ttu-id="9ac5b-109">Директива</span><span class="sxs-lookup"><span data-stu-id="9ac5b-109">Directive</span></span>         | <span data-ttu-id="9ac5b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9ac5b-110">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac5b-111">realm</span><span class="sxs-lookup"><span data-stu-id="9ac5b-111">realm</span></span>             | <span data-ttu-id="9ac5b-112">Определяемое реализацией указание для клиента о том, какие [*учетные данные*](/windows/desktop/SecGloss/c-gly) требуются.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-112">An implementation-defined hint to the client about which [*credentials*](/windows/desktop/SecGloss/c-gly) are required.</span></span> <span data-ttu-id="9ac5b-113">Клиент должен отобразить эти сведения пользователю, если он запрашивает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-113">The client should display this information to the user if it is prompting for credentials.</span></span>                                                  |
| <span data-ttu-id="9ac5b-114">алгоритм</span><span class="sxs-lookup"><span data-stu-id="9ac5b-114">algorithm</span></span>         | <span data-ttu-id="9ac5b-115">Microsoft Digest поддерживает MD5 и MD5-подряд.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-115">Microsoft Digest supports MD5 and MD5-Sess.</span></span> <span data-ttu-id="9ac5b-116">Для оптимальной производительности используйте MD5-подряд.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-116">For optimal performance, use MD5-Sess.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="9ac5b-117">коп</span><span class="sxs-lookup"><span data-stu-id="9ac5b-117">qop</span></span>               | <span data-ttu-id="9ac5b-118">Для этой директивы можно задать значение AUTH, auth-int или auth-CONF.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-118">This directive can be set to auth, auth-int, or auth-conf.</span></span> <span data-ttu-id="9ac5b-119">Дополнительные сведения см. в разделе [качество защиты и шифров](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="9ac5b-119">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="9ac5b-120">nonce</span><span class="sxs-lookup"><span data-stu-id="9ac5b-120">nonce</span></span>             | <span data-ttu-id="9ac5b-121">Уникальное закодированное значение, созданное сервером для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-121">A unique encoded value generated by the server for each challenge.</span></span> <span data-ttu-id="9ac5b-122">Клиент не должен изменять это значение.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-122">This value must not be altered by the client.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="9ac5b-123">непрозрачный</span><span class="sxs-lookup"><span data-stu-id="9ac5b-123">opaque</span></span>            | <span data-ttu-id="9ac5b-124">Содержит ссылку на установленный [*контекст безопасности*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="9ac5b-124">Contains a reference for the [*security context*](/windows/desktop/SecGloss/s-gly) that is being established.</span></span> <span data-ttu-id="9ac5b-125">Дополнительные сведения см. [в разделе поддержание контекста безопасности между соединениями](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="9ac5b-125">For more information, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span> |
| <span data-ttu-id="9ac5b-126">шифр (только SASL)</span><span class="sxs-lookup"><span data-stu-id="9ac5b-126">cipher(SASL only)</span></span> | <span data-ttu-id="9ac5b-127">Список шифров, поддерживаемых сервером.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-127">The list of ciphers that the server supports.</span></span> <span data-ttu-id="9ac5b-128">Этот элемент может присутствовать в дайджесте SASL, только если директива КОП указывает auth-CONF.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-128">This element can be present in a Digest SASL challenge only if the qop directive specifies auth-conf.</span></span> <span data-ttu-id="9ac5b-129">Дополнительные сведения см. в разделе [качество защиты и шифров](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="9ac5b-129">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                              |
| <span data-ttu-id="9ac5b-130">charset</span><span class="sxs-lookup"><span data-stu-id="9ac5b-130">charset</span></span>           | <span data-ttu-id="9ac5b-131">Для этой директивы можно задать значение UTF-8, если сервер может обрабатывать имена пользователей и сферы в кодировке UTF-8.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-131">This directive can be set to utf-8 if the server can process UTF-8–encoded user names and realms.</span></span> <span data-ttu-id="9ac5b-132">Если клиент понимает директиву charset, он может ответить, используя значения в кодировке UTF-8.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-132">If the client understands the charset directive, it can respond by using UTF-8–encoded values.</span></span>                                                                                                       |



 

<span data-ttu-id="9ac5b-133">Microsoft Digest формирует строку запроса дайджеста для серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="9ac5b-133">Microsoft Digest generates the Digest challenge string for server applications.</span></span> <span data-ttu-id="9ac5b-134">Дополнительные сведения см. [в разделе Создание дайджест-запроса](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="9ac5b-134">For details, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
