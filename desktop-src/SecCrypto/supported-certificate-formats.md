---
description: Список форматов сертификатов, поддерживаемых службами сертификации.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Поддерживаемые форматы сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663437"
---
# <a name="supported-certificate-formats"></a><span data-ttu-id="2286c-103">Поддерживаемые форматы сертификатов</span><span class="sxs-lookup"><span data-stu-id="2286c-103">Supported Certificate Formats</span></span>

<span data-ttu-id="2286c-104">Службы сертификатов могут выдавать сертификаты следующих типов.</span><span class="sxs-lookup"><span data-stu-id="2286c-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="2286c-105">Термин</span><span class="sxs-lookup"><span data-stu-id="2286c-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="2286c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2286c-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2286c-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Сертификат проверки подлинности клиента [*X. 509*](../secgloss/x-gly.md) версии 3, совместимый с SSL</span><span class="sxs-lookup"><span data-stu-id="2286c-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="2286c-108">Этот сертификат проверки подлинности клиента идентифицирует клиента и используется серверами для проверки подлинности клиента, запрашивающего доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="2286c-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="2286c-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Сертификат проверки подлинности сервера X. 509 v3, совместимый с SSL</span><span class="sxs-lookup"><span data-stu-id="2286c-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="2286c-110">Этот сертификат проверки подлинности сервера идентифицирует сервер и используется клиентами для проверки подлинности сервера, к которому клиент хочет получить доступ.</span><span class="sxs-lookup"><span data-stu-id="2286c-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="2286c-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Сертификат [*S/MIME*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="2286c-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="2286c-112">Этот сертификат используется клиентами для защиты электронной почты по протоколу S/MIME (Secure/Multiprotocol Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="2286c-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="2286c-113">Помимо этих сертификатов, службы сертификации также можно использовать для выдаче других сертификатов X. 509 путем написания настраиваемого модуля политики.</span><span class="sxs-lookup"><span data-stu-id="2286c-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="2286c-114">Условия "сертификат проверки подлинности сервера" и "сертификат сервера", а также "сертификат проверки подлинности клиента" и "сертификат клиента" являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="2286c-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="2286c-115">Кроме того, службы сертификатов включают шаблоны сертификатов в конфигурации центра сертификации предприятия Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2286c-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="2286c-116">Чтобы понять, как определяются сертификаты, обратитесь к справочной документации Windows по шаблонам сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2286c-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
