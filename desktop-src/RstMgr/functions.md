---
title: Функции диспетчера перезапуска
description: API диспетчера перезапуска использует функции, указанные в следующей таблице.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Диспетчер перезапуска, ссылка, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d628fcd5c1f6488d69152340dd76ae59ac27ea93b2ca157179a052883a26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010202"
---
# <a name="restart-manager-functions"></a>Функции диспетчера перезапуска

API диспетчера перезапуска использует функции, указанные в следующей таблице.



| Функция                                           | Описание                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**рмаддфилтер**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Изменяет действия завершения работы или перезапуска.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Запускает новый сеанс диспетчера перезапуска.                                                                                                                                                        |
| [**рмжоинсессион**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Присоединяет процесс приложения к существующему сеансу диспетчера перезапуска.                                                                                                                  |
| [**рмендсессион**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Завершает сеанс диспетчера перезапуска.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Регистрирует ресурсы, такие как имена файлов, короткие имена служб или [**уникальные структуры \_ \_ процессов RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , в сеансе диспетчера перезапуска.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Используется установщиками для получения списка всех приложений, затронутых зарегистрированными ресурсами, и их текущим состоянием.                                                                              |
| [**рмжетфилтерлист**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Запрашивает состояние завершения работы и перезапускает уже примененные изменения.                                                                                                     |
| [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Инициирует завершение работы приложений и служб.                                                                                                                                        |
| [**рмремовефилтер**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Удаляет уже примененные изменения для завершения работы и перезапуска.                                                                                                                   |
| [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Перезапускает приложения и службы, работа которых была завершена функцией [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) и которые были зарегистрированы для перезапуска с помощью **регистераппликатионрестарт**. |
| [**рмканцелкурренттаск**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Отменяет текущую функцию [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .                                                            |



 

 

 




