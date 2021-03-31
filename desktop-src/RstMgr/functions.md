---
title: Функции диспетчера перезапуска
description: API диспетчера перезапуска использует функции, указанные в следующей таблице.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Диспетчер перезапуска, ссылка, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888203"
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



 

 

 




