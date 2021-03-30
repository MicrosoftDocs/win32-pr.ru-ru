---
description: Страница глоссария
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Глоссарий (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910847"
---
# <a name="glossary-winhttp"></a><span data-ttu-id="e4ab7-103">Глоссарий (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="e4ab7-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="e4ab7-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**данные проверки подлинности**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-105">Зависящий от схемы блок данных, которыми обмениваются сервер и клиент во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="e4ab7-106">Чтобы доказать свою личность, Клиент шифрует некоторые или все эти данные с помощью имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="e4ab7-107">Клиент отправляет зашифрованные данные на сервер, который расшифровывает данные и сравнивает их с исходным.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="e4ab7-108">Если расшифрованные данные соответствуют исходным данным, клиент проходит проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**кодировка Base64**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-110">Схема, используемая для передачи двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="e4ab7-111">Base64 обрабатывает данные в виде 24-разрядных групп, сопоставляя эти данные с четырьмя закодированными символами.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="e4ab7-112">Иногда ее называют кодировкой 3 – 4.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="e4ab7-113">Каждый 6 бит 24-разрядной группы используется в качестве индекса в таблице сопоставления (в кодировке Base64) для получения символа для закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="e4ab7-114">Длина закодированных данных ограничена 76 символами.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**хранилище сертификатов**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-116">Обычно хранится постоянное хранилище, в котором хранятся сертификаты, списки отзыва сертификатов (CRL) и списки доверия сертификатов (CTL).</span><span class="sxs-lookup"><span data-stu-id="e4ab7-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="e4ab7-117">Хранилище сертификатов также может быть временным при работе с сертификатами на основе сеанса.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**Cobranding**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-119">Способность сайта-участника Microsoft Passport предоставлять собственные элементы фирменной символики и объяснения на страницах сетевой службы Passport.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="e4ab7-120">Софирменная символика включает в себя настройку внешнего вида, конкретного текста и конкретного поведения для страниц сети Passport.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**Кодовая страница**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-122">Таблица, связывающая двоичные коды символов, используемые программой, с клавишами на клавиатуре или с видом символов на мониторе.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="e4ab7-123">Использование кодовых страниц — это способ обеспечить поддержку наборов символов и раскладок клавиатуры, используемых в разных странах и регионах.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="e4ab7-124">Можно настроить такие устройства, как монитор и клавиатура, для использования определенной кодовой страницы и переключения с одной кодовой страницы (например, США) на другую (например, Португалия) по запросу пользователя.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP-команда**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-126">HTTP-команда (или метод HTTP) является инструкцией, отправленной в сообщении запроса, которое уведомляет HTTP-сервер о действии, выполняемом с указанным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="e4ab7-127">Например, "GET" указывает, что ресурс извлекается с сервера.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="e4ab7-128">Общие команды включают "GET", "POST" и "HEAD".</span><span class="sxs-lookup"><span data-stu-id="e4ab7-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="e4ab7-129">Дополнительные сведения и полный список стандартных HTTP-команд см. в спецификации HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**службу**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-131">Файл cookie, содержащий профиль пользователя для проверки подлинности Passport.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="e4ab7-132">Каждый билет соответствует одному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="e4ab7-133">Сервер входа в доменный центр Passport предоставляет билеты, которые клиент отправляет члену Passport для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="e4ab7-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**агент пользователя**</span><span class="sxs-lookup"><span data-stu-id="e4ab7-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="e4ab7-135">Агент пользователя — это клиентское приложение, запрашивающее документ с HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="e4ab7-136">Когда клиент отправляет запрос на HTTP-сервер, обычно он отправляет имя агента пользователя в заголовок запроса, чтобы сервер мог определить возможности клиентского программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e4ab7-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 



