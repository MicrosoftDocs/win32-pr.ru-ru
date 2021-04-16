---
description: Объясняет использование токенов олицетворения в контроле доступа.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Токены олицетворения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664305"
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

 

 
