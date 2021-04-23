---
title: Строки UrlPrefix
description: В API сервера HTTP UrlPrefix — это строка Юникода с расширенными символами (UTF-16) с канонической формой, которая указывает раздел пространства имен URL-адреса.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- UrlPrefix строки API сервера HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797203"
---
# <a name="urlprefix-strings"></a><span data-ttu-id="f1173-104">Строки UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="f1173-104">UrlPrefix Strings</span></span>

<span data-ttu-id="f1173-105">В API сервера HTTP *UrlPrefix* — это строка Юникода с расширенными символами (UTF-16) с канонической формой, которая указывает раздел пространства имен URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f1173-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="f1173-106">Он используется для резервирования раздела пространства имен URL-адреса для учетной записи пользователя или регистрации раздела пространства имен URL-адреса для процесса.</span><span class="sxs-lookup"><span data-stu-id="f1173-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="f1173-107">Формат UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="f1173-107">UrlPrefix Format</span></span>

<span data-ttu-id="f1173-108">UrlPrefix имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="f1173-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="f1173-109">"схема://Host: порт/relativeURI"</span><span class="sxs-lookup"><span data-stu-id="f1173-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="f1173-110">Элементы схемы, узла и порта UrlPrefix должны быть представлены и не быть пустыми и должны соблюдать следующие правила.</span><span class="sxs-lookup"><span data-stu-id="f1173-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="f1173-111"><span id="scheme"></span><span id="SCHEME"></span>Схема</span><span class="sxs-lookup"><span data-stu-id="f1173-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="f1173-112">Значение должно быть либо HTTP, либо HTTPS, в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="f1173-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="f1173-113"><span id="host"></span><span id="HOST"></span>хост</span><span class="sxs-lookup"><span data-stu-id="f1173-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="f1173-114">Необходимо указать полное доменное имя, строку литерала IPv4 или IPv6 или подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="f1173-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="f1173-115">В отличие от схемы, которая должна быть строчной, часть узла не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="f1173-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="f1173-116">В зависимости от того, как указана его часть узла, UrlPrefix попадает в одну из четырех категорий маршрутизации, которые более подробно описаны ниже:</span><span class="sxs-lookup"><span data-stu-id="f1173-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="f1173-117">Строгий шаблон</span><span class="sxs-lookup"><span data-stu-id="f1173-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="f1173-118">Явная</span><span class="sxs-lookup"><span data-stu-id="f1173-118">Explicit</span></span></dd> <dd><span data-ttu-id="f1173-119">Слабый шаблон с ограниченным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="f1173-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="f1173-120">Слабый шаблон</span><span class="sxs-lookup"><span data-stu-id="f1173-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="f1173-121"><span id="port"></span><span id="PORT"></span>порту</span><span class="sxs-lookup"><span data-stu-id="f1173-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="f1173-122">Десятичная числовая строка, которая не начинается с нуля и представляет допустимый номер TCP-порта (от 1 до 65 535).</span><span class="sxs-lookup"><span data-stu-id="f1173-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="f1173-123">Это значение не может быть подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="f1173-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="f1173-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="f1173-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="f1173-125">Элемент relativeURI является необязательным, но при его наличии всегда должен следовать символ косой черты ("/").</span><span class="sxs-lookup"><span data-stu-id="f1173-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="f1173-126">Это строка префикса, указывающая поддерево в пространстве имен компьютера, указанное относительно значения схемы, узла и порта.</span><span class="sxs-lookup"><span data-stu-id="f1173-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="f1173-127">В отличие от схемы, которая должна быть строчной, часть relativeURI не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="f1173-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="f1173-128">Примеры правильно сформированных Урлпрефиксес:</span><span class="sxs-lookup"><span data-stu-id="f1173-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="f1173-129">Категории Host-Specifier</span><span class="sxs-lookup"><span data-stu-id="f1173-129">Host-Specifier Categories</span></span>

<span data-ttu-id="f1173-130">Для гибкости и простоты использования API сервера HTTP поддерживает четыре разных способа указания узлов.</span><span class="sxs-lookup"><span data-stu-id="f1173-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="f1173-131">Четыре категории спецификаторов узлов перечислены ниже в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="f1173-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="f1173-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Строгий шаблон (знак "плюс")</span><span class="sxs-lookup"><span data-stu-id="f1173-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="f1173-133">Если ведущий элемент UrlPrefix состоит из одного знака плюса (+), UrlPrefix сопоставляет все возможные имена узлов в контексте его схемы, порта и элемента relativeURI и попадает в категорию строгого шаблона.</span><span class="sxs-lookup"><span data-stu-id="f1173-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="f1173-134">Строгий шаблон полезен, если приложению требуется обслуживать запросы, адресованные одному или нескольким Релативеурис, независимо от того, как эти запросы поступают на компьютер или какой сайт они указал в заголовках узлов.</span><span class="sxs-lookup"><span data-stu-id="f1173-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="f1173-135">Использование строгого подстановочного знака в этой ситуации позволяет избежать необходимости указывать исчерпывающий список узлов и/или IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f1173-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="f1173-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Прямая</span><span class="sxs-lookup"><span data-stu-id="f1173-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="f1173-137">Явное имя узла, например полное доменное имя в элементе Host, помещает UrlPrefix в явную категорию.</span><span class="sxs-lookup"><span data-stu-id="f1173-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="f1173-138">Этот тип ведущего элемента сопоставляется непосредственно с заголовками узлов входящих запросов.</span><span class="sxs-lookup"><span data-stu-id="f1173-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="f1173-139">Явные спецификации узлов полезны для приложений с несколькими сайтами, таких как веб-серверы, которые доставляют различные ресурсы в зависимости от сайта, на который был направлен запрос.</span><span class="sxs-lookup"><span data-stu-id="f1173-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="f1173-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Слабый шаблон с ограниченным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="f1173-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="f1173-141">Когда IP-адрес отображается как ведущий элемент, UrlPrefix попадает в неограниченную IP-маску.</span><span class="sxs-lookup"><span data-stu-id="f1173-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="f1173-142">Этот тип UrlPrefix соответствует любому имени узла для указанного IP-интерфейса с указанной схемой, портом и relativeURI и не соответствует строгому шаблону или явному UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="f1173-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="f1173-143">IP-адрес принимает одну из двух форм в элементе Host:</span><span class="sxs-lookup"><span data-stu-id="f1173-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="f1173-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Строка литерала IPv4</span><span class="sxs-lookup"><span data-stu-id="f1173-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="f1173-145">Литерал IPv4 состоит из четырех десятичных чисел с точками в диапазоне 0-255, например 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="f1173-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="f1173-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Строка литерала IPv6</span><span class="sxs-lookup"><span data-stu-id="f1173-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="f1173-147">Строка литерала IPv6 заключена в квадратные скобки и содержит шестнадцатеричные числа, разделенные двоеточиями. Например:: \[ : 1 \] или \[ 3FFE: FFFF:: 6ECB: 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="f1173-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="f1173-148">Спецификаторы узлов с слабым шаблоном с ограниченным IP-адресом предназначены для приложений, которые зависят от маршрута, принимаемого входящими запросами.</span><span class="sxs-lookup"><span data-stu-id="f1173-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="f1173-149">Не следует полагаться на спецификаторы узлов с ограниченным использованием IP-адресов, чтобы обеспечить безопасность.</span><span class="sxs-lookup"><span data-stu-id="f1173-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="f1173-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Слабый символ-шаблон (звездочка)</span><span class="sxs-lookup"><span data-stu-id="f1173-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="f1173-151">Когда в \* качестве ведущего элемента отображается звездочка (), UrlPrefix попадает в категорию слабых подстановочных знаков.</span><span class="sxs-lookup"><span data-stu-id="f1173-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="f1173-152">Этот тип UrlPrefix соответствует любому имени узла, связанному с указанной схемой, портом и параметром relativeURI, который еще не совпал с слабым шаблоном UrlPrefix с нестрогим подстановочным знаком, явным образом или с IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="f1173-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="f1173-153">В некоторых обстоятельствах эту спецификацию узла можно использовать по умолчанию, а также можно использовать для указания большого раздела пространства имен URL-адресов без использования многих Урлпрефиксес.</span><span class="sxs-lookup"><span data-stu-id="f1173-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="f1173-154">Обнаружение конфликтов UrlPrefix во время резервирования и регистрации</span><span class="sxs-lookup"><span data-stu-id="f1173-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="f1173-155">В целях резервирования и регистрации четыре различные категории UrlPrefix обрабатываются отдельно, без ссылки на друг друга.</span><span class="sxs-lookup"><span data-stu-id="f1173-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="f1173-156">Можно зарегистрировать конфликтующие Урлпрефиксес, если они находятся в разных категориях.</span><span class="sxs-lookup"><span data-stu-id="f1173-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="f1173-157">Конфликт в пределах одной категории вызывает сбой попытки резервирования.</span><span class="sxs-lookup"><span data-stu-id="f1173-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="f1173-158">Например, можно зарезервировать как явные UrlPrefix `https://www.adatum.com:80/vroot/` , так и конфликтующие строгие подстановочные знаки UrlPrefix `https://+:80/vroot/` , так как они принадлежат разным категориям.</span><span class="sxs-lookup"><span data-stu-id="f1173-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="f1173-159">Однако последующая попытка зарезервировать https://+:80/vroot/ другого пользователя завершится ошибкой, так как это приведет к конфликту с существующим резервированием в собственной категории.</span><span class="sxs-lookup"><span data-stu-id="f1173-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="f1173-160">Поведение маршрутизации</span><span class="sxs-lookup"><span data-stu-id="f1173-160">Routing Behavior</span></span>

<span data-ttu-id="f1173-161">При маршрутизации входящего HTTP-запроса API сервера HTTP начинается с категории строгого шаблона и сравнивает входящий URL-адрес с зарегистрированными и зарезервированными Урлпрефиксес в этой категории.</span><span class="sxs-lookup"><span data-stu-id="f1173-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="f1173-162">Если входящий URL-адрес совпадает с резервированием, но не с регистрацией, то API сервера HTTP не сможет выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f1173-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="f1173-163">Это предотвращает возможность получения запросов, не предназначенных для него, с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="f1173-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="f1173-164">Состояние ошибки — 400 ("Недопустимый запрос"), а не 503 ("Служба недоступна"), так как возвращаемое значение 503 иногда ошибочно интерпретируется шлюзами балансировки нагрузки, как указано, что сервер перегружен.</span><span class="sxs-lookup"><span data-stu-id="f1173-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="f1173-165">Если в категории найдена соответствующая регистрация, запрос направляется в очередь запросов, связанную с этой регистрацией.</span><span class="sxs-lookup"><span data-stu-id="f1173-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="f1173-166">Запрос всегда направляется в очередь, связанную с наиболее длинными UrlPrefix в категории.</span><span class="sxs-lookup"><span data-stu-id="f1173-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="f1173-167">Если в категории не найдено совпадений, API сервера HTTP переходит к явной категории и повторяет ту же процедуру.</span><span class="sxs-lookup"><span data-stu-id="f1173-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="f1173-168">Чтобы суммировать, порядок, в котором анализируются категории, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1173-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="f1173-169">Строгий шаблон</span><span class="sxs-lookup"><span data-stu-id="f1173-169">Strong wildcard</span></span>
2.  <span data-ttu-id="f1173-170">Явная</span><span class="sxs-lookup"><span data-stu-id="f1173-170">Explicit</span></span>
3.  <span data-ttu-id="f1173-171">IP-Bound слабый шаблон</span><span class="sxs-lookup"><span data-stu-id="f1173-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="f1173-172">Слабый шаблон</span><span class="sxs-lookup"><span data-stu-id="f1173-172">Weak wildcard</span></span>

<span data-ttu-id="f1173-173">Если в какой-либо из категорий совпадений не найдено, API сервера HTTP отправляет ответ с кодом состояния 400, указывая на то, что запрос не может быть перенаправлен.</span><span class="sxs-lookup"><span data-stu-id="f1173-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="f1173-174">Правило наиболее подходящие</span><span class="sxs-lookup"><span data-stu-id="f1173-174">Longest Match Rule</span></span>

<span data-ttu-id="f1173-175">В каждой категории UrlPrefix API сервера HTTP направляет запрос в очередь, связанную с самым длинным UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="f1173-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="f1173-176">Например, предположим, что следующие две Урлпрефиксес зарегистрированы в разных очередях:</span><span class="sxs-lookup"><span data-stu-id="f1173-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="f1173-177">API сервера HTTP направляет запрос `https://www.adatum.com:80/default.htm` на Queue1 и запрос `https://www.adatum.com:80/dir/sna/snadefault.htm` на Queue2.</span><span class="sxs-lookup"><span data-stu-id="f1173-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="f1173-178">Он направляет запрос `https://www.adatum.com:80/dir/app.htm` на Queue1, так как самое длинное полное соответствие заключается в `https://www.adatum.com:80/` UrlPrefix, а не в `https://www.adatum.com:80/dir/sna` UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="f1173-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




