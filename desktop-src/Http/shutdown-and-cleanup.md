---
title: Завершение работы и очистка
description: Для корректного завершения работы приложения необходимо выполнить следующие операции очистки.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a551ad57ddbf63c6ff598814794bc5837da646e98169d8250e543575abd013a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950694"
---
# <a name="shutdown-and-cleanup"></a>Завершение работы и очистка

Для корректного завершения работы приложения необходимо выполнить следующие операции очистки:

-   Удалите все зарегистрированные URL-адреса из группы URL-адресов, вызвав функцию [**хттпремовеурлфромурлграуп**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) для отмены регистрации URL-адресов, ранее зарегистрированных в вызове [**хттпаддурлтаурлграуп**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Закройте группу URL-адресов, вызвав функцию [**хттпклосеурлграуп**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) . Перед закрытием сеанса сервера необходимо закрыть все группы URL-адресов, созданные в сеансе сервера.
-   Закройте сеанс сервера, вызвав [**хттпклосесерверсессион**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Закройте рукоятку очереди запросов, вызвав [**хттпклосерекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Завершите ресурсы, созданные API-сервером HTTP, вызвав функцию [**хттптерминате**](/windows/desktop/api/Http/nf-http-httpterminate) с совпадающими параметрами флагов для каждого вызова приложения, созданного в [**хттпинитиализе**](/windows/desktop/api/Http/nf-http-httpinitialize). Каждый из этих вызовов завершает все ресурсы, созданные в вызове [**хттпинитиализе**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




