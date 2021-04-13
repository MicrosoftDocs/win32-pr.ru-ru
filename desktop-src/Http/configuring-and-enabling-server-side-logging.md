---
title: Настройка и включение ведения журнала на стороне сервера
description: Настройка и включение ведения журнала на стороне сервера
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410926"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Настройка и включение ведения журнала на стороне сервера

Приложение включает ведение журнала в сеансе сервера или в группе URL-адресов перед отправкой ответа с помощью [**хттпсендхттпреспонсе**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). В следующем примере показано, как настроить и включить ведение журнала на стороне сервера типа W3C.

1.  Приложение инициализирует структуру [**\_ ведения журнала HTTP \_**](/windows/desktop/api/Http/ns-http-http_logging_info) с помощью **HttpLoggingTypeW3C** , указанной в элементе **Format** , и битовую маску констант [**\_ \_ поля журнала HTTP**](http-log-field--constants.md) в элементе **Fields** .
2.  Приложение вызывает [**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) или [**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) с **хттпсерверлоггингпроперти** , указанным в параметре *Property* , и указателем на [**структуру \_ \_ сведений о ведении журнала HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info) в параметре *pPropertyInformation* .

Битовая маска констант [**\_ \_ поля журнала HTTP**](http-log-field--constants.md) содержит поля, которые могут быть зарегистрированы в файле журнала W3C. Обратите внимание, что установка свойства **хттпсерверлоггингпроперти** в сеансе сервера или в группе URL-адресов не означает, что будут регистрироваться HTTP-ответы. Ведение журнала выполняется для каждого запроса, когда в вызове [**хттпсендхттпреспонсе**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) или [**хттпсендреспонсинтитибоди**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)включен W3C.

Чтобы включить ведение журнала ответов W3C на основе каждого запроса, приложение выполняет следующие действия:

1.  Приложение инициализирует элементы [**\_ \_ \_ данных полей журнала HTTP**](/windows/desktop/api/Http/ns-http-http_log_fields_data) данными поля, которое будет зарегистрировано для этого ответа.
2.  **Базовый член. Type** структуры [**\_ \_ \_ данных полей журнала HTTP**](/windows/desktop/api/Http/ns-http-http_log_fields_data) должен инициализироваться в **хттплогдататипефиелдс**. Поле **base. Type** обеспечивает дальнейшее расширение структуры и API.
3.  Приложение вызывает [**хттпсендхттпреспонсе**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) или [**хттпсендреспонсинтитибоди**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) с указателем на структуру [**\_ \_ \_ данных полей журнала HTTP**](/windows/desktop/api/Http/ns-http-http_log_fields_data) в параметре *плогдата* . Приложение должно выполнить приведение указателя к [**\_ \_ данным журнала ФТТП**](/windows/desktop/api/Http/ns-http-http_log_data).

 

 




