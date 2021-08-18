---
title: Run-Timeные функции для запрашивающих сторона EAPHost
description: Сведения о функциях времени выполнения EAPHost, таких как Еафостпирбегинсессион и Еафостпиржетресулт.
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97481347535de03cb1d3c04f341f382c270f0ae89482060e9952c38cfbdc5b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785332"
---
# <a name="eaphost-supplicant-run-time-functions"></a>Run-Timeные функции для запрашивающих сторона EAPHost

Функции времени выполнения API для запрашивающего устройства EAP приведены ниже.



| Функция                                                                     | Описание                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | Запускает сеанс проверки подлинности EAP.                                                                                                                                                                                |
| [**еафостпирклеарконнектион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | Останавливает все будущие обратные вызовы к [**нотификатионхандлер**](/previous-versions/windows/desktop/api) , предоставляемому вызывающим абонентом, в EAPHost в предыдущем вызове [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession). |
| [**еафостпирендсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | Завершает текущий сеанс проверки подлинности EAP между EAPHost и вызывающим запрашивающим.                                                                                                                          |
| [**еафостпирфриеаперрор**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | Освобождает все модули памяти, относящиеся к ошибкам EAP, возвращаемые API-интерфейсами EAPHost.                                                                                                                                                        |
| [**еафостфрирунтимемемори**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | Высвобождает пространство памяти, используемое интерфейсами API времени выполнения.                                                                                                                                                                         |
| [**еафостпиржетаусстатус**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | Получает текущее состояние проверки подлинности EAP от EAPHost.                                                                                                                                             |
| [**еафостпиржетидентити**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | Запрашивает сведения об идентификаторе из внутренних методов.                                                                                                                                                                |
| [**еафостпиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | Получает массив атрибутов проверки подлинности EAP от EAPHost.                                                                                                                                                      |
| [**еафостпиржетресулт**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | Получает результат проверки подлинности для указанного сеанса проверки подлинности EAP.                                                                                                                                      |
| [**еафостпиржетсендпаккет**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | Получает пакет от EAPHost для отправки в средство проверки подлинности.                                                                                                                                                          |
| [**еафостпиржетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | Получает контекст пользовательского интерфейса для запрашивающего сторона от EAPHost, который используется в API-интерфейсах [**еафостпиринвокеинтерактивеуи**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) для данного запрашивающего устройства.                             |
| [**еафостпиринитиализе**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | Инициализирует EAPHost для запрашивающего устройства. [**Еафостинитиализе**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) и [**еафостунинитиализе**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) должны вызываться как пары.                                      |
| [**еафостпирпроцессрецеиведпаккет**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | Передает пакет EAP в EAPHost после получения пакета EAP с сервера.                                                                                                                             |
| [**еафостпирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | Предоставляет обновленные атрибуты проверки подлинности EAP для EAPHost.                                                                                                                                                           |
| [**еафостпирсетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | Предоставляет новый или обновленный контекст пользовательского интерфейса для однорангового метода EAP, загруженного на EAPHost.                                                                                                                           |
| [**еафостпирунинитиализе**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Унитиализес EapHost для данного запрашивающего устройства. [**Еафостинитиализе**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) и [**еафостунинитиализе**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) должны вызываться как пары.                                      |



 

 

 




