---
title: Создание безопасного клиента или сервера RPC
description: В этом разделе приводятся рекомендации по написанию безопасного клиента RPC или сервера.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Удаленный вызов процедур RPC, рекомендации, написание безопасного клиента или сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b752d8dab216691105e428833c83bce28b974f121ddcc77861fbb6671d72dd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010392"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Создание безопасного клиента или сервера RPC

В этом разделе приводятся рекомендации по написанию безопасного клиента RPC или сервера.

сведения в этом разделе относятся к Windows 2000 и Windows XP. Этот раздел относится ко всем последовательностям протоколов, включая [**нкалрпк**](/windows/desktop/Midl/ncalrpc). Разработчики, как правило, считают, что **нкалрпк** не является потенциальной целью для атаки, что неверно на сервере терминалов, где потенциально сотни пользователей имеют доступ к службе, что может привести к появлению дополнительного доступа.

Этот раздел состоит из следующих разделов:

-   [Используемый поставщик безопасности](which-security-provider-to-use.md)
-   [Управление проверкой подлинности клиента](controlling-client-authentication.md)
-   [Выбор уровня проверки подлинности](choosing-an-authentication-level.md)
-   [Выбор параметров качества обслуживания для системы безопасности](choosing-security-qos-options.md)
-   [Распространенная ошибка: допущение Рпксерверрегистераусинфо предотвращает вызов сервера неавторизованными пользователями](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Обратные вызовы](callbacks.md)
-   [Сеансы со значением NULL](null-sessions.md)
-   [Использование флага/robust](use-the-robust-flag.md)
-   [Методы IDL для лучшего проектирования интерфейсов и методов](idl-techniques-for-better-interface-and-method-design.md)
-   [Строгое и строго типизированные дескрипторы контекста](strict-and-type-strict-context-handles.md)
-   [Не доверять одноранговому узлу](do-not-trust-your-peer.md)
-   [Не использовать безопасность конечных точек](do-not-use-endpoint-security.md)
-   [Будьте осторожны с другими конечными точками RPC, работающими в том же процессе](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Проверьте, Кто ли сервер утвержден](verify-the-server-is-who-it-claims-to-be.md)
-   [Использование основных последовательностей протоколов](use-mainstream-protocol-sequences.md)
-   [Насколько защищен мой RPC-сервер?](how-secure-is-my-rpc-server-now.md)

 

 