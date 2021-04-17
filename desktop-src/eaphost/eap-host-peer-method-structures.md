---
title: Структуры одноранговых методов EAPHost
description: Сведения о структурах API одноранговых методов EAPHost, таких как Еапцертификатекредентиал и Еапсимкредентиал.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691666"
---
# <a name="eaphost-peer-method-structures"></a>Структуры одноранговых методов EAPHost

Ниже приведены структуры API одноранговых методов EAPHost.



| Структура                                                              | Описание                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**еапцертификатекредентиал**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Содержит сведения о сертификате, используемом методом EAP для проверки подлинности.                                                                                                            |
| [**еапкредентиал**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Содержит сведения о типе учетных данных и соответствующих учетных данных. Он передается в качестве входных данных в API [**еаппиржетконфигблобандусерблоб**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) . |
| [**\_подпрограммы метода одноранговых \_ методов EAP \_**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Содержит набор указателей на функции API однорангового метода EAPHost.                                                                                                                               |
| [**еаппирмесодаутпут**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Содержит сведения о действии, возвращаемом методом однорангового узла EAP.                                                                                                                                    |
| [**еаппирмесодресулт**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Содержит результирующие данные, созданные методом EAP во время проверки подлинности.                                                                                                                             |
| [**еапсимкредентиал**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Содержит сведения о SIM-карте, используемой методом EAP для проверки подлинности.                                                                                                              |
| [**еапусернамепассвордкредентиал**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Содержит имя пользователя и пароль, используемые методом EAP для проверки подлинности пользователя.                                                                                                     |



 

 

 




