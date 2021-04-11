---
title: Завершение работы и очистка
description: Для корректного завершения работы приложения необходимо выполнить следующие операции очистки.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068079"
---
# <a name="shutdown-and-cleanup"></a>Завершение работы и очистка

Для корректного завершения работы приложения необходимо выполнить следующие операции очистки:

-   Удалите все зарегистрированные URL-адреса из группы URL-адресов, вызвав функцию [**хттпремовеурлфромурлграуп**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) для отмены регистрации URL-адресов, ранее зарегистрированных в вызове [**хттпаддурлтаурлграуп**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Закройте группу URL-адресов, вызвав функцию [**хттпклосеурлграуп**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) . Перед закрытием сеанса сервера необходимо закрыть все группы URL-адресов, созданные в сеансе сервера.
-   Закройте сеанс сервера, вызвав [**хттпклосесерверсессион**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Закройте рукоятку очереди запросов, вызвав [**хттпклосерекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Завершите ресурсы, созданные API-сервером HTTP, вызвав функцию [**хттптерминате**](/windows/desktop/api/Http/nf-http-httpterminate) с совпадающими параметрами флагов для каждого вызова приложения, созданного в [**хттпинитиализе**](/windows/desktop/api/Http/nf-http-httpinitialize). Каждый из этих вызовов завершает все ресурсы, созданные в вызове [**хттпинитиализе**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




