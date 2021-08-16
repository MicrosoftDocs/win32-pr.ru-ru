---
description: Описание вызовов, необходимых для создания сертификата.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Создание сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e497f20e8a20d4e401ce89a85d1f8a312dad76865a6c3dfb523d8f2526125c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772979"
---
# <a name="building-a-certificate"></a>Создание сертификата

Порядок вызова в сборке сертификата выглядит следующим образом:

1.  [*Центр сертификации*](../secgloss/c-gly.md) (ЦС) инициализирует модули с помощью вызовов [**ицертполици**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) и [**ицертексит**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (происходит один раз при инициализации сервера). ЦС инициализирует модули политики и выхода, вызывая [**ICertPolicy2:: Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) и [**Ицертексит:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  Посредник вызывает ЦС через [**ицертконфиг**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (происходит один раз для каждой промежуточной инициализации). Промежуточный носитель находит необходимую строку конфигурации путем вызова [**ицертконфиг:: config**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  Клиент вызывает посредника через интерфейс, относящийся к промежуточному посреднику (происходит один раз для каждого запроса). Клиент отправляет запрос на [*сертификат*](../secgloss/c-gly.md) промежуточному посреднику. это может быть, например, Microsoft Internet Explorer, который отправляет запрос через [управление регистрацией сертификатов](certificate-enrollment-control.md) для Microsoft IIS.
4.  Посредник в ЦС через [**интерфейса ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (происходит один раз для каждого запроса). Посредник отправляет запрос сертификата в ЦС через [**интерфейса ICertRequest:: submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit). в случае службы IIS это можно сделать с помощью скриптов Active Server страниц.
5.  ЦС вызывает модуль политики через интерфейс [**ицертполици**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (происходит один раз для каждого запроса). Центр сертификации уведомляет модуль политики о том, что запрос пришел путем вызова [**ицертполици:: верифирекуест**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest). Модуль политики может проверить запрос и изменить сертификат, вызвав методы интерфейса [**ицертсерверполици**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . После этого модуль политики может указать, что запрос будет "ОК" (если это так, сертификат будет создан на этом этапе), запрос будет отклонен или запрос должен быть приостановлен.
6.  Используемых Администратор вызывает ЦС через интерфейс [**ицертадмин**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) . Если запрос приостановлен, администратор может повторно отправить или отклонить запрос либо изменить атрибуты и расширения запроса. Обратите внимание, что если запрос повторно отправляется, модуль политики будет иметь еще одну возможность обработки запроса (в результате вызова [**ицертполици:: верифирекуест**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). Задача повторной отправки или отклонения запроса может выполняться с помощью оснастки MMC центра сертификации или другого приложения, использующего **ицертадмин**.
7.  ЦС вызывает модуль Exit через интерфейс [**ицертексит**](/windows/desktop/api/Certexit/nn-certexit-icertexit) . Если в модуле выхода указано (при вызове [**ицертексит:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) на шаге 1), что он заинтересован в отображении выданных сертификатов или ожидающих запросов, ЦС вызывает [**Ицертексит:: notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  Модуль выхода вызывает ЦС через интерфейс [**ицертсерверексит**](/windows/desktop/api/Certif/nn-certif-icertserverexit) . Модуль выхода может проверить запрос и новый сертификат, вызвав методы **ицертсерверексит**.

 

 
