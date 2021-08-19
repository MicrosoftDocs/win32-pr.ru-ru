---
description: сервер с \_ привилегией SE TCB \_ имени, например служба Windows, работающая в учетной записи LocalSystem, может вызвать функцию LogonUser для проверки подлинности клиента на компьютере, на котором выполняется сервер.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Сеансы входа клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783026"
---
# <a name="client-logon-sessions"></a>Сеансы входа клиента

сервер с \_ привилегией SE TCB \_ имени, например служба Windows, работающая в [учетной записи LocalSystem](/windows/desktop/Services/localsystem-account), может вызвать функцию [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) для [*проверки подлинности*](/windows/desktop/SecGloss/a-gly) клиента на компьютере, на котором выполняется сервер. Функция **LogonUser** запускает новый [*сеанс*](/windows/desktop/SecGloss/s-gly) входа в систему и возвращает [*основной маркер доступа*](/windows/desktop/SecGloss/p-gly) , содержащий сведения о безопасности клиента. Этот первичный токен можно использовать при вызове функции [**имперсонателогжедонусер**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) для олицетворения клиента или при вызове функции [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) для создания процесса, который выполняется в [*контексте безопасности*](/windows/desktop/SecGloss/s-gly) клиента.

Преимущество проверки подлинности клиента заключается в том, что сервер, олицетворяющий прошедший проверку подлинности клиент или [*процесс*](/windows/desktop/SecGloss/p-gly) , созданный в контексте аутентифицированного клиента, может подключаться к удаленным сетевым ресурсам в качестве клиента. Если такая проверка подлинности не выполнена, сервер может подключаться к сетевым ресурсам только в том случае, если он получил имя и пароль учетной записи клиента для передачи функции [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .

Недостаток проверки подлинности клиента заключается в том, что сервер должен получить [*учетные данные*](/windows/desktop/SecGloss/c-gly) клиента (доменное имя, имя пользователя и пароль). Если удаленный клиент передает эти учетные данные на сервер, то ответственность за передачу учетных данных в безопасном режиме обеспечивает клиент и сервер.

 

 
