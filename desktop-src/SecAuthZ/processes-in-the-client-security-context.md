---
description: Серверное приложение может вызвать функцию параметр CreateProcessAsUser, чтобы создать новый процесс, выполняемый в контексте безопасности клиентов.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Процессы в контексте Client Security
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650566"
---
# <a name="processes-in-the-client-security-context"></a>Процессы в контексте Client Security

Серверное приложение может вызвать функцию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) , чтобы создать новый процесс, выполняемый в [*контексте безопасности*](/windows/desktop/SecGloss/s-gly)клиента. При вызове с [*маркером доступа*](/windows/desktop/SecGloss/a-gly)клиента **параметр CreateProcessAsUser** требует \_ привилегий SE ассигнпримаритокен \_ Name и SE \_ увеличить \_ имя квоты \_ , которые хранятся в службах Windows, работающих в [учетной записи LocalSystem](/windows/desktop/Services/localsystem-account).

Для функции [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) также требуется [*основной маркер доступа*](/windows/desktop/SecGloss/p-gly). Сервер может получить основной маркер доступа для клиента либо путем [запуска сеанса входа](client-logon-sessions.md) для клиента, либо путем [олицетворения клиента](client-impersonation.md) и дублирования [*маркера олицетворения*](/windows/desktop/SecGloss/i-gly).

В следующих процедурах описаны два способа создания клиентского процесса.

**Создание клиентского процесса путем входа на клиент**

1.  Заносить клиент на локальный компьютер, используя [*учетные данные*](/windows/desktop/SecGloss/c-gly) клиента при вызове функции [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera). **LogonUser** создает основной маркер для [*сеанса входа*](/windows/desktop/SecGloss/l-gly)клиента.
2.  Если сервер должен использовать контекст безопасности клиента, получите доступ к исполняемому файлу для клиентского [*процесса*](/windows/desktop/SecGloss/p-gly) с помощью первичного маркера в вызове функции [**имперсонателогжедонусер**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .
3.  Создайте процесс в контексте безопасности клиента с помощью основного маркера в вызове [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).

> [!Note]  
> Процесс, созданный с помощью следующего метода, может не иметь доступа к сетевым ресурсам, если он не содержит [*учетные данные*](/windows/desktop/SecGloss/c-gly)клиента.

 

**Создание клиентского процесса путем олицетворения клиента**

1.  Запустите олицетворение с помощью функции олицетворения, например [**имперсонатенамедпипеклиент**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient).
2.  Вызовите функцию [**опенсреадтокен**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , чтобы получить маркер олицетворения с контекстом безопасности клиента.
3.  Вызовите функцию [**дупликатетокенекс**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) , чтобы преобразовать токен олицетворения в основной токен.
4.  Используйте основной маркер в вызове функции [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) , чтобы создать процесс в контексте безопасности клиента.

По умолчанию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) создает клиентский [*процесс*](/windows/desktop/SecGloss/p-gly) на неинтерактивных оконных станциях и настольных системах. Чтобы создать интерактивный процесс, сервер должен сначала задать [*избирательные списки управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL) для интерактивной рабочей станции и рабочего стола, чтобы убедиться, что клиенту разрешен доступ к ним. Предпочтительным способом сделать это является запись клиента в журнал, [Получение идентификатора безопасности (SID) сеанса входа клиента](/previous-versions//aa446670(v=vs.85)), а затем использование этого идентификатора SID в разрешенных для доступа элементах ACE как на интерактивной рабочей станции, так и на рабочем столе. Затем сервер может вызвать **параметр CreateProcessAsUser**, указав интерактивную станцию окон и настольную winsta0 \\ по умолчанию. Пример, демонстрирующий эту процедуру, см. [в разделе Запуск интерактивного клиентского процесса на C++](/previous-versions//aa379608(v=vs.85)).

 

 
