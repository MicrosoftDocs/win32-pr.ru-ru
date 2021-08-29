---
title: Удостоверение конечной точки
description: Типы, определенные в этом разделе, используются для определения идентификатора безопасности адреса конечной точки.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Веб-службы удостоверения конечной точки для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819fd2b33f1c74f88ef9032a49bd9aa4f04e34f1dcd4e599120951afabb6e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927594"
---
# <a name="endpoint-identity"></a>Удостоверение конечной точки

Типы, определенные в этом разделе, используются для определения идентификатора безопасности адреса конечной точки.

Следующие элементы API являются частью отступов конечной точки:



| Перечисление                                                       | Описание                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**\_тип удостоверения конечной точки WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | Тип удостоверения конечной точки, используемый в качестве селектора для подтипов [**\_ \_ удостоверения конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity). |



 



| Структура                                                               | Описание                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ удостоверение КОНЕЧНОЙ точки WS CERT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | Тип удостоверения конечной точки сертификата.                                                 |
| [**\_ \_ удостоверение конечной точки DNS WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | Тип для указания удостоверения конечной точки, представленного DNS-именем.                      |
| [**\_удостоверение конечной точки WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | Базовый тип для всех идентификаторов конечных точек.                                                   |
| [**\_ \_ удостоверение КОНЕЧНОЙ точки WS RSA \_**](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | Введите идентификатор конечной точки RSA.                                                              |
| [**\_ \_ удостоверение конечной точки имени участника-службы WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | Тип для указания удостоверения конечной точки, представленного именем участника-службы (SPN). |
| [**WS — \_ неизвестное \_ \_ удостоверение конечной точки**](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | Тип для идентификатора неизвестной конечной точки.                                                   |
| [**\_ \_ удостоверение конечной точки имени участника-пользователя \_**](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | Тип для указания удостоверения конечной точки, представленного именем участника-пользователя.     |



 

 

 




