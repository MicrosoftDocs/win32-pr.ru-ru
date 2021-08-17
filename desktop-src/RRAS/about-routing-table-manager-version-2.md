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
ms.openlocfilehash: c87228222f31daf7f951064d05c92d950a3fff0d570fcac3536887b50193b16b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792111"
---
# <a name="about-routing-table-manager-version-2"></a>Сведения о диспетчере таблиц маршрутизации версии 2

В следующей документации описывается технология диспетчера таблиц маршрутизации версии 2 (RTMv2). API RTMv2 — это компонент Windows 2000 и более поздних операционных систем, которые можно использовать для записи протоколов маршрутизации, взаимодействующих с диспетчером таблиц маршрутизации.

Диспетчер таблиц маршрутизации является центральным репозиторием сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).

RTMv2 недоступен для Windows NT версии 4,0. кроме того, RTMv2 нельзя использовать для протоколов IPX-маршрутизации, работающих на Windows NT 4,0 или Windows 2000. при использовании протокола IPX или записи протоколов маршрутизации для Windows NT 4,0 обратитесь к статье [о маршрутизации диспетчера таблиц версии 1](about-routing-table-manager-version-1.md).

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

 

 




