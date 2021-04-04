---
description: Защищенный сервер может использовать следующие функции для создания отчетов об аудите в журнале событий безопасности.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Аудит доступа к частным объектам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3669841714fe9c24f6346404bc8634222bc4557e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999674"
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



 

 

 
