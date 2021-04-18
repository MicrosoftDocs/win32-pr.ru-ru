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
# <a name="url"></a>Url

Элементы API URL-адреса ВВСАПИ предоставляют механизмы для разбиения и декодирования URL-адресов в части компонентов, а также для экранирования и объединения частей компонентов обратно в URL-адрес.

-   Чтобы разделить и разбить URL-адреса на части компонентов, используйте функцию [**всдекодеурл**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .
-   Для экранирования и объединения частей компонентов обратно в URL-адрес используется функция [**всенкодеурл**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .
-   Чтобы объединить относительные URL-адреса с абсолютным базовым URL-адресом, формирующим абсолютный URL, используйте функцию [**вскомбинеурл**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .

Следующие перечисления являются частью URL-адреса:

-   [**\_Флаги URL-адреса WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_тип схемы URL-адресов WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

Следующие функции являются частью URL-адреса:

-   [**вскомбинеурл**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**всдекодеурл**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**всенкодеурл**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

Следующие структуры являются частью URL-адреса:

-   [**\_ \_ URL-адрес WS HTTPS**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**\_ \_ URL-адрес WS HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**\_ \_ URL-адрес WS нетпипе**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_ \_ URL-адрес WS NETTCP**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**\_ \_ URL-адрес WS соапудп**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**\_URL-адрес WS**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




