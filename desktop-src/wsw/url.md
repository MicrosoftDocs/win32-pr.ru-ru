---
title: Url
description: Элементы API URL-адреса ВВСАПИ предоставляют механизмы для разбиения и декодирования URL-адресов в части компонентов, а также для экранирования и объединения частей компонентов обратно в URL-адрес.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Веб-службы URL для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2020
ms.locfileid: "105700815"
---
# <a name="url"></a><span data-ttu-id="b6cef-106">Url</span><span class="sxs-lookup"><span data-stu-id="b6cef-106">Url</span></span>

<span data-ttu-id="b6cef-107">Элементы API URL-адреса ВВСАПИ предоставляют механизмы для разбиения и декодирования URL-адресов в части компонентов, а также для экранирования и объединения частей компонентов обратно в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b6cef-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="b6cef-108">Чтобы разделить и разбить URL-адреса на части компонентов, используйте функцию [**всдекодеурл**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .</span><span class="sxs-lookup"><span data-stu-id="b6cef-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="b6cef-109">Для экранирования и объединения частей компонентов обратно в URL-адрес используется функция [**всенкодеурл**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .</span><span class="sxs-lookup"><span data-stu-id="b6cef-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="b6cef-110">Чтобы объединить относительные URL-адреса с абсолютным базовым URL-адресом, формирующим абсолютный URL, используйте функцию [**вскомбинеурл**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .</span><span class="sxs-lookup"><span data-stu-id="b6cef-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="b6cef-111">Следующие перечисления являются частью URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="b6cef-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="b6cef-112">**\_Флаги URL-адреса WS \_**</span><span class="sxs-lookup"><span data-stu-id="b6cef-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="b6cef-113">**\_тип схемы URL-адресов WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b6cef-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="b6cef-114">Следующие функции являются частью URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="b6cef-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="b6cef-115">**вскомбинеурл**</span><span class="sxs-lookup"><span data-stu-id="b6cef-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="b6cef-116">**всдекодеурл**</span><span class="sxs-lookup"><span data-stu-id="b6cef-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="b6cef-117">**всенкодеурл**</span><span class="sxs-lookup"><span data-stu-id="b6cef-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="b6cef-118">Следующие структуры являются частью URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="b6cef-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="b6cef-119">**\_ \_ URL-адрес WS HTTPS**</span><span class="sxs-lookup"><span data-stu-id="b6cef-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="b6cef-120">**\_ \_ URL-адрес WS HTTP**</span><span class="sxs-lookup"><span data-stu-id="b6cef-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="b6cef-121">**\_ \_ URL-адрес WS нетпипе**</span><span class="sxs-lookup"><span data-stu-id="b6cef-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="b6cef-122">**\_ \_ URL-адрес WS NETTCP**</span><span class="sxs-lookup"><span data-stu-id="b6cef-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="b6cef-123">**\_ \_ URL-адрес WS соапудп**</span><span class="sxs-lookup"><span data-stu-id="b6cef-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="b6cef-124">**\_URL-адрес WS**</span><span class="sxs-lookup"><span data-stu-id="b6cef-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




