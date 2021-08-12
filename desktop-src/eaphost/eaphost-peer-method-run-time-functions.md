---
title: Run-Time функции однорангового метода EAPHost
description: Сведения о функциях времени выполнения API одноранговых методов EAPHost. Просмотрите список функций и просмотрите дополнительные доступные ресурсы.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3134a2b118b4bce4511e79d8d9ef58708f6b1c2bd7a93ed820fc16ec073914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275027"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Run-Time функции однорангового метода EAPHost

Функции времени выполнения API однорангового метода EAP приведены ниже.



| Компонент                                                                   | Описание                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Запускает новый сеанс проверки подлинности на одноранговом узле EAPHost.                                                                                                                                                                    |
| [**еаппирендсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Завершает текущий сеанс проверки подлинности EAP между EAPHost и одноранговым узлом.                                                                                                                                               |
| [**еаппиржетконфигблобандусерблоб**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Позволяет разработчикам методов EAP предоставлять различные свойства соединения и пользовательские свойства, поддерживаемые методом. EAPHost вызывает эту функцию для создания свойства соединения и пользовательского свойства метода EAP. |
| [**еаппиржетидентити**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Получает удостоверение для метода EAP, вызывающего.                                                                                                                                                                    |
| [**еаппиржетинфо**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Получает набор указателей на функцию для реализации загруженного однорангового метода EAP.                                                                                                                                     |
| [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Получает массив атрибутов EAP из метода EAP.                                                                                                                                                                     |
| [**еаппиржетреспонсепаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Получает ответный пакет от метода EAP.                                                                                                                                                                              |
| [**еаппиржетресулт**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Получает результат сеанса проверки подлинности из метода EAP.                                                                                                                                                        |
| [**еаппиржетуиконтекст**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Получает контекст пользовательского интерфейса из метода EAP.                                                                                                                                                                     |
| [**еаппиринитиализе**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Инициализирует EAPHost для однорангового метода.                                                                                                                                                                                    |
| [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Обрабатывает пакет, полученный с помощью EAPHost, от запрашивающей стороны.                                                                                                                                                                   |
| [**еаппирсеткредентиалс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Предоставляет новые или обновленные учетные данные пользователя для метода EAP.                                                                                                                                                                 |
| [**еаппирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Предоставляет обновленный массив атрибутов EAP методу EAP.                                                                                                                                                              |
| [**еаппирсетуиконтекст**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Предоставляет контекст пользовательского интерфейса для метода EAP.                                                                                                                                                                        |
| [**еаппиршутдовн**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Завершает работу метода EAP и готовится к выгрузке соответствующей библиотеки DLL.                                                                                                                                                     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции настройки однорангового метода EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




