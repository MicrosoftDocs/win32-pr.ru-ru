---
title: Настройка сеанса сервера
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681380"
---
# <a name="configuring-the-server-session"></a>Настройка сеанса сервера

Идентификатор сеанса сервера создается с помощью функции [**хттпкреатесерверсессион**](/windows/desktop/api/Http/nf-http-httpcreateserversession) и используется в вызове [**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). Параметр *ппропертинформатион* указывает на структуру конфигурации для заданного типа свойства. Параметр *пропертинформатионленгс* задает размер (в байтах) структуры конфигурации. Например, при задании параметра **хттпсервертимеаутспроперти** параметр **ппропертинформатион** должен указывать на буфер, который не меньше размера структуры данных [**\_ \_ \_ об ограничении времени ожидания HTTP**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

Обычно приложение HTTP создает сеанс с одним сервером и может устанавливать свойства уровня приложения, такие как ограничение глобальной полосы пропускания или включить централизованное ведение журнала в этом сеансе сервера. [**Хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) переопределяет конфигурации API-сервера HTTP для вызывающего приложения; Он не влияет на свойства HTTP-сервера на уровне API. Запросы к конфигурациям сеансов сервера запрашиваются путем вызова [**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




