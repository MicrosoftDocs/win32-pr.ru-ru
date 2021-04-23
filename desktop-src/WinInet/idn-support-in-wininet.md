---
title: Поддержка IDN в WinINet
description: Начиная с Windows Server 2008 и Windows Vista, часть узла URL-адреса в Юникоде преобразуется в международного доменного имени (IDN).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413525"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="8ae9a-103">Поддержка IDN в WinINet</span><span class="sxs-lookup"><span data-stu-id="8ae9a-103">IDN Support in WinINet</span></span>

<span data-ttu-id="8ae9a-104">Начиная с Windows Server 2008 и Windows Vista, часть узла URL-адреса в Юникоде преобразуется в международного доменного имени (IDN).</span><span class="sxs-lookup"><span data-stu-id="8ae9a-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="8ae9a-105">Отдельные части кодировки URL-адресов в Юникоде также могут быть изменены конфигурациями, заданными приложением.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="8ae9a-106">Версии ANSI API WinINet продолжают отсылать URL-адрес по каналу, указанному приложением, однако версии API WinINet в Юникоде теперь соответствуют стандарту IDN (RFC3490) для кодировок URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="8ae9a-107">По умолчанию при вводе URL-адреса в качестве параметра в формате Юникод часть узла, как для прокси-сервера, так и для прямых подключений, преобразуется в формат IDN.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="8ae9a-108">Приложение имеет возможность отключить форматирование узла IDN, задав параметр **Интернета \_ \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="8ae9a-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="8ae9a-109">Преобразование узла IDN можно включить только для прямых или прокси-подключений с помощью флага **Internet \_ Flag \_ IDN \_ Direct** или **Internet \_ флаг \_ IDN \_ -прокси** с **\_ параметром Интернета \_ IDN**.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="8ae9a-110">В следующем примере кода показано, как отключить преобразование узла IDN как для прокси-сервера, так и для прямых соединений.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="8ae9a-111">Если форматирование узла IDN отключено, приложение может указать нужную кодовую страницу, используя **\_ \_ кодовую страницу параметра Интернета**.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="8ae9a-112">В следующем примере кода показано, как задать японскую кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="8ae9a-113">Часть пути URL-адреса по умолчанию кодируется в кодировке UTF8, а остальные сегменты URL-адреса, запроса или фрагмента преобразуются в системную кодовую страницу по умолчанию (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="8ae9a-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="8ae9a-114">В следующем примере показано, как указать кодовую страницу корейского языка для части пути URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="8ae9a-115">В следующей таблице описаны параметры, поддерживающие IDN.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="8ae9a-116">Дополнительные сведения см. в разделе ["флаги параметров](option-flags.md) ".</span><span class="sxs-lookup"><span data-stu-id="8ae9a-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="8ae9a-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="8ae9a-117">Option</span></span>                            | <span data-ttu-id="8ae9a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8ae9a-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae9a-119">\_Страница параметров \_ Интернета</span><span class="sxs-lookup"><span data-stu-id="8ae9a-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="8ae9a-120">Этот параметр задается в запросе или в обработчике соединения, чтобы указать схему кодировки кодовой страницы для части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="8ae9a-121">Этот параметр игнорируется, если включен IDN.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="8ae9a-122">\_ \_ путь к странице параметров Интернета \_</span><span class="sxs-lookup"><span data-stu-id="8ae9a-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="8ae9a-123">Этот параметр задается в запросе, или обработчик соединения включает указанную схему кодировки для части пути URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="8ae9a-124">По умолчанию часть пути URL-адреса кодируется в кодировке UTF8.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="8ae9a-125">\_ \_ Вспомогательная страница параметра Интернета \_</span><span class="sxs-lookup"><span data-stu-id="8ae9a-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="8ae9a-126">Установка этого параметра для запроса или маркера подключения включает указанную схему кодировки для дополнительной части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="8ae9a-127">По умолчанию вспомогательная часть URL-адреса кодируется в системную кодовую страницу по умолчанию (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="8ae9a-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="8ae9a-128">\_параметр Интернета \_ IDN</span><span class="sxs-lookup"><span data-stu-id="8ae9a-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="8ae9a-129">Этот параметр можно использовать в запросе или в обработчике соединения для включения или отключения преобразования узла IDN.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="8ae9a-130">Если IDN отключены, WinINet использует системную кодовую страницу по умолчанию для кодирования части узла или центра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="8ae9a-131">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="8ae9a-132">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="8ae9a-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8ae9a-133">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8ae9a-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 