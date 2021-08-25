---
description: Объясняет использование токенов олицетворения в контроле доступа.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Токены олицетворения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67acf48a1f274703850fc8bfc2167014708124c46743f416591510b6c9ab559b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908144"
---
# <a name="impersonation-tokens"></a>Токены олицетворения

Поток олицетворения имеет два [*маркера доступа*](/windows/desktop/SecGloss/a-gly):

-   [*Основной маркер доступа*](/windows/desktop/SecGloss/p-gly) , описывающий [*контекст безопасности*](/windows/desktop/SecGloss/s-gly) сервера. Чтобы получить маркер для этого маркера, вызовите функцию [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .
-   Маркер доступа олицетворения, описывающий контекст безопасности олицетворенного клиента. Чтобы получить маркер для этого маркера, вызовите функцию [**опенсреадтокен**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .

Сервер может использовать [*токен олицетворения*](/windows/desktop/SecGloss/i-gly) в следующих функциях:

-   В функциях [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**акцессчеккбитипе**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)и [**акцессчеккбитипересултлист**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , чтобы определить, позволяет ли [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) клиента использовать набор прав доступа.
-   В функции [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы включить или отключить права клиента.
-   В функции [**привилежечекк**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) , чтобы определить, включен ли набор привилегий в маркере клиента.
-   В функциях, создающих записи в журнале событий безопасности, например [**обжектопенаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) или [**привилежедсервицеаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Эти функции используют токен олицетворения для получения сведений о клиенте для записи журнала.

 

 
