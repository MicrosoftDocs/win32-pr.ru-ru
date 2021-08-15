---
title: Функции настройки однорангового метода EAPHost
description: Дополнительные сведения о функциях настройки однорангового метода EAPHost. Просмотрите список функций настройки и просмотрите дополнительные доступные ресурсы.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355784647be6c6e13d4110303d544670e80ce09e7f9f99be02b662205e8ead82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785199"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Функции настройки однорангового метода EAPHost

Функции настройки API однорангового метода EAP приведены ниже.



| Функция                                                                                                  | Описание                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Преобразует большой двоичный объект конфигурации в формат XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Преобразует XML в большой двоичный объект конфигурации.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Преобразует учетные данные XML в большой двоичный объект.                                                                                                                                                                                                                            |
| [**еаппирфриеррормемори**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Освобождает все модули памяти, относящиеся к ошибкам EAP, возвращенные одноранговые API-интерфейсы EapHost.                                                                                                                                                                                               |
| [**еаппирфримемори**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Освобождает всю память, выделенную с помощью параметров OUT метода EAP.                                                                                                                                                                                                      |
| [**еаппиринвокеконфигуи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Вызывает в клиенте диалоговое окно пользовательского интерфейса настройки подключения для метода EAP.                                                                                                                                                                   |
| [**еаппиринвокеидентитюи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Создает настраиваемое диалоговое окно интерактивного пользовательского интерфейса для получения сведений об удостоверении пользователя для метода EAP на клиенте.                                                                                                                                          |
| [**еаппиринвокеинтерактивеуи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Создает настраиваемое диалоговое окно интерактивного пользовательского интерфейса для метода EAP на клиенте.                                                                                                                                                                              |
| [**еаппиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Определяет реализацию функции, зависящей от метода EAP, которая получает поля ввода учетных данных для единого входа EAP (SSO) для этого метода EAP.                                                                                                              |
| [**еаппиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Определяет реализацию функции бесобъектного взаимодействия EAP, которая получает поля ввода для интерактивных компонентов пользовательского интерфейса, которые вызываются на запрашивающем.                                                                                                     |
| [**еаппиркуерюиблобфроминтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Преобразует сведения о пользователе в большой двоичный объект пользователя, который может использоваться функциями времени выполнения EAPHost.                                                                                                                                                                   |
| [**еаппиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Определяет реализацию функции, зависящей от метода EAP, которая создает большой двоичный объект учетных данных пользователя EAP из структуры [**\_ \_ массива входных полей конфигурации EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) , содержащей данные об учетных данных, предоставленные пользователем-ответчиком. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Run-Time функции однорангового метода EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




