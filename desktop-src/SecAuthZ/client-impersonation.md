---
description: Олицетворение — это способность потока выполняться с использованием разных сведений о безопасности, отличных от процесса, владеющего потоком.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Олицетворение клиента (авторизация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454e943b53cffbc4430c71b31e2b172095b999e2201c4cafc08b081bf1782e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783070"
---
# <a name="client-impersonation-authorization"></a>Олицетворение клиента (авторизация)

[*Олицетворение*](/windows/desktop/SecGloss/i-gly) — это способность потока выполняться с использованием разных сведений о безопасности, отличных от процесса, владеющего потоком. Как правило, поток в серверном приложении олицетворяет клиента. Это позволяет серверному потоку действовать от имени этого клиента для доступа к объектам на сервере или проверки доступа к собственным объектам клиента.

Microsoft Windows API предоставляет следующие функции для начала олицетворения.

-   Приложение сервера DDE может вызывать функцию [**ддеимперсонатеклиент**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) для олицетворения клиента.
-   Сервер именованных каналов может вызывать функцию [**имперсонатенамедпипеклиент**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) .
-   Для олицетворения контекста безопасности [*маркера доступа*](/windows/desktop/SecGloss/a-gly)пользователя, выполнившего вход, можно вызвать функцию [**имперсонателогжедонусер**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .
-   Функция [**имперсонатеселф**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) позволяет потоку создавать копию собственного маркера доступа. Это полезно, когда приложению необходимо изменить контекст безопасности одного потока. Например, иногда необходимо включить [*привилегию*](/windows/desktop/SecGloss/p-gly)только для одного потока процесса.
-   Можно вызвать функцию [**сетсреадтокен**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) , чтобы целевой поток выполнялся в контексте безопасности указанного [*токена олицетворения*](/windows/desktop/SecGloss/i-gly).
-   Серверное приложение удаленного вызова процедур (RPC) Майкрософт может вызывать функцию [**рпЦимперсонатеклиент**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) для олицетворения клиента.
-   [*Пакет безопасности*](/windows/desktop/SecGloss/s-gly) или сервер приложений может вызывать функцию [**имперсонатесекуритиконтекст**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) для олицетворения клиента.

Для большинства этих олицетворений поток олицетворения может вернуться к своему собственному контексту безопасности, вызвав функцию [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) . Исключением является олицетворение RPC, при котором сервер RPC вызывает [**рпкреверттоселф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) или [**рпкреверттоселфекс**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) для возврата к собственному контексту безопасности.

 

 
