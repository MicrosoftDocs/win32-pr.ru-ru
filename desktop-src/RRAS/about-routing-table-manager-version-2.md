---
title: Сведения о диспетчере таблиц маршрутизации версии 2
description: В следующей документации описывается технология диспетчера таблиц маршрутизации версии 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации версии 2
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации версии 2, описание
- Диспетчер таблиц маршрутизации, служба RRAS версии 2
- Диспетчер таблиц маршрутизации, версия 2 RRAS, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068096"
---
# <a name="about-routing-table-manager-version-2"></a>Сведения о диспетчере таблиц маршрутизации версии 2

В следующей документации описывается технология диспетчера таблиц маршрутизации версии 2 (RTMv2). API RTMv2 — это компонент Windows 2000 и более поздних операционных систем, которые можно использовать для записи протоколов маршрутизации, взаимодействующих с диспетчером таблиц маршрутизации.

Диспетчер таблиц маршрутизации является центральным репозиторием сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).

RTMv2 недоступен для Windows NT версии 4,0. Кроме того, RTMv2 нельзя использовать для протоколов IPX-маршрутизации, работающих в Windows NT 4,0 или Windows 2000. При использовании протокола IPX или записи протоколов маршрутизации для Windows NT 4,0 обратитесь к статье [о маршрутизации диспетчера таблиц версии 1](about-routing-table-manager-version-1.md).

В этом обзоре описываются следующие темы:

-   [Компоненты архитектуры диспетчера таблиц маршрутизации](components-of-the-routing-table-manager-architecture.md)
-   [Регистрация в диспетчере таблиц маршрутизации](registering-with-the-routing-table-manager.md)
-   [Перечисление зарегистрированных сущностей](enumerating-registered-entities.md)
-   [Использование методов](using-methods.md)
-   [Использование непрозрачных указателей](using-opaque-pointers.md)
-   [Маркировка маршрутов для состояния Hold-Down](marking-routes-for-the-hold-down-state.md)
-   [Добавление маршрутов](adding-routes.md)
-   [Получение сведений о маршруте](retrieving-route-information.md)
-   [Обновление маршрутов](updating-routes.md)
-   [Получение уведомлений об изменениях](receiving-notification-of-changes.md)
-   [Работа со следующими прыжками](working-with-next-hops.md)
-   [Перечисление записей таблицы маршрутизации](enumerating-routing-table-entries.md)
-   [Поиск конкретных сведений в таблице маршрутизации](finding-specific-information-in-the-routing-table.md)
-   [Обслуживание списков Client-Specific](maintaining-client-specific-lists.md)
-   [Управление дескрипторами](managing-handles.md)

 

 




