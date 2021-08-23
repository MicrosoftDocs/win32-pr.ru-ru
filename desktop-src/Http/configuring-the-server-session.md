---
title: Настройка сеанса сервера
description: Настройка сеанса сервера
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d2710a0d9a0f7f3c70ad6de84336d382ae161b938ee2e22f20ddde5012604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746594"
---
# <a name="configuring-the-server-session"></a>Настройка сеанса сервера

Идентификатор сеанса сервера создается с помощью функции [**хттпкреатесерверсессион**](/windows/desktop/api/Http/nf-http-httpcreateserversession) и используется в вызове [**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). Параметр *ппропертинформатион* указывает на структуру конфигурации для заданного типа свойства. Параметр *пропертинформатионленгс* задает размер (в байтах) структуры конфигурации. Например, при задании параметра **хттпсервертимеаутспроперти** параметр **ппропертинформатион** должен указывать на буфер, который не меньше размера структуры данных [**\_ \_ \_ об ограничении времени ожидания HTTP**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

Обычно приложение HTTP создает сеанс с одним сервером и может устанавливать свойства уровня приложения, такие как ограничение глобальной полосы пропускания или включить централизованное ведение журнала в этом сеансе сервера. [**Хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) переопределяет конфигурации API-сервера HTTP для вызывающего приложения; Он не влияет на свойства HTTP-сервера на уровне API. Запросы к конфигурациям сеансов сервера запрашиваются путем вызова [**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




