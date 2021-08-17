---
description: Защищенный сервер может использовать следующие функции для создания отчетов об аудите в журнале событий безопасности.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Аудит доступа к частным объектам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac3a38a9f0af292a77a539491e0cea5f1faf40b570f34a35371ad43a7abe757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784595"
---
# <a name="auditing-access-to-private-objects"></a>Аудит доступа к частным объектам

Защищенный сервер может использовать следующие функции для создания отчетов об аудите в журнале событий безопасности.



| Функция                                                                                                     | Описание                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**акцессчеккандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | То же, что и функция [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , за исключением того, что она может формировать сообщения аудита для неудачных или успешных попыток доступа.                                                                            |
| [**акцессчеккбитипеандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | То же, что и функция [**акцессчеккбитипе**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) , за исключением того, что она может формировать сообщения аудита для неудачных или успешных попыток доступа.                                                                |
| [**акцессчеккбитипересултлистандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | То же, что и функция [**акцессчеккбитипересултлист**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , за исключением того, что она может формировать сообщения аудита для неудачных или успешных попыток доступа.                                            |
| [**акцессчеккбитипересултлистандаудиталармбихандле**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | То же, что и функция [**акцессчеккбитипересултлистандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) , за исключением того, что она позволяет вызывающему потоку выполнять проверку доступа до олицетворения клиента. |
| [**обжектклосеаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Формирует сообщение аудита, указывающее, что клиент пытался закрыть закрытый объект.                                                                                                                                   |
| [**обжектделетеаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Формирует сообщение аудита, указывающее, что клиент пытался удалить закрытый объект.                                                                                                                                  |
| [**обжектопенаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Формирует сообщение аудита, указывающее, что клиент пытался открыть или создать закрытый объект.                                                                                                                          |
| [**обжектпривилежеаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Формирует сообщение аудита, указывающее, что клиент пытался использовать указанный набор привилегий в сочетании с попыткой доступа к закрытому объекту.                                                              |
| [**привилежедсервицеаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Формирует сообщение аудита, указывающее, что клиент пытался использовать указанный набор привилегий.                                                                                                                        |



 

 

 
