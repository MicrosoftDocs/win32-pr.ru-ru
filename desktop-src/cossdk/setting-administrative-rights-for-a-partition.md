---
description: Установка прав администратора для секции
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Установка прав администратора для секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807360"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Установка прав администратора для секции

Пользователям, которым назначена роль администратора системного приложения COM+, разрешено создавать, изменять и удалять разделы COM+. В средстве администрирования «службы компонентов» административные роли можно назначать пользователям, развернув папку « **роли** » системного приложения COM+.

Начиная с Windows Server 2003, функция проверки подлинности для системного приложения COM+ включает значение ЕОАК \_ disable \_ AAA. Это значение, которое отключает активацию активации на основе активатора (AAA), используется в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) при запуске системного приложения. Установка функции проверки подлинности в ЕОАК \_ disable \_ AAA позволяет приложению, работающему под привилегированной учетной записью (например, LocalSystem), предотвратить использование удостоверения для запуска ненадежных компонентов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сбор метрик секции](collecting-partition-metrics.md)
</dt> <dt>

[Настройка кэша секций](configuring-the-partition-cache.md)
</dt> <dt>

[Группирование приложений в секции](grouping-applications-into-partitions.md)
</dt> <dt>

[Управление локальными секциями](managing-local-partitions.md)
</dt> <dt>

[Управление секциями в Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
