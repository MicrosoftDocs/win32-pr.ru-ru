---
title: Последовательность вызовов API однорангового метода
description: Сведения о последовательности вызовов API однорангового метода. См. список, демонстрирующий последовательность вызовов, выполненных с помощью EAPHost для однорангового метода EAP.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042792"
---
# <a name="peer-method-api-call-sequence"></a>Последовательность вызовов API однорангового метода

В этом разделе содержится конкретная последовательность вызовов для API однорангового метода. Во время обычного сеанса проверки подлинности EAP EAPHost вызывает ряд вызовов методов EAP для реализации API однорангового метода EAPHost.

В следующем списке показана последовательность вызовов, выполненных с помощью EAPHost, для однорангового метода EAP.

-   Загружает библиотеку DLL однорангового метода EAP, используемую для проверки подлинности.
-   Вызывает [**еаппиржетинфо**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) для метода, чтобы получить список указателей на функции, реализованные в библиотеке DLL. Предполагается, что последующие вызовы функций, выполняемые одноранговым объектом EAPHost (клиентом), были реализованы в библиотеке DLL.
-   Вызывает [**еаппиринитиализе**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) , чтобы указать библиотеке методов EAP подготовить по крайней мере один сеанс проверки подлинности с помощью этого однорангового метода.
-   Вызывает [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) , чтобы установить уникальный сеанс проверки подлинности.
-   Вызывает [**еаппиржетидентити**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) , чтобы получить удостоверение, используемое для проверки подлинности. Если удостоверение недоступно или пользователь должен предоставить дополнительные сведения, то EAPHost вызывает [ **еаппиржетуиконтекст.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Эта функция получает сведения о контексте для диалогового окна пользовательского интерфейса, которое будет создано на запрашивающем сторона. После того, как пользователь отправил сведения об удостоверении, удостоверение пользователя задается вызовом [**еаппирсетуиконтекст**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)и получается путем вызова **еаппиржетидентити**.
-   Повторяет следующие шаги, пока [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) не указывает, что результат проверки подлинности доступен.
    -   Вызывает [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) с указателем пакета запроса для передачи в вызывающий объект.
    -   Вызывает **еаппиржетреспонсепаккет** , чтобы получить пакет ответа для отправки в средство проверки подлинности.
    -   При необходимости, если необходимо получить или отправить атрибуты EAP во время сеанса проверки подлинности, EAPHost вызывает [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) и [**еаппирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) соответственно.
-   Когда средство проверки подлинности отправляет код действия, который указывает на завершение проверки подлинности, EAPHost вызывает [**еаппиржетресулт**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) и получает результаты проверки подлинности.
-   Вызывает [**еаппирендсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) для завершения сеанса проверки подлинности.
-   Вызывает [**еаппиршутдовн**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) для выгрузки библиотеки DLL однорангового метода.
-   Выгружает библиотеку методов EAP.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Последовательность вызовов API-интерфейса для запрашивающих сторон](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator Последовательность вызовов API метода](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Последовательности вызовов EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




