---
description: Установка прав администратора для секции
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Установка прав администратора для секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33431c5beff76e015d28b6a7e886823620126f2ed9b84db68af9a8f3b8ac1d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915827"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Установка прав администратора для секции

Пользователям, которым назначена роль администратора системного приложения COM+, разрешено создавать, изменять и удалять разделы COM+. В средстве администрирования «службы компонентов» административные роли можно назначать пользователям, развернув папку « **роли** » системного приложения COM+.

начиная с Windows Server 2003, функция проверки подлинности для системного приложения COM+ включает значение еоак \_ DISABLE \_ AAA. Это значение, которое отключает активацию активации на основе активатора (AAA), используется в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) при запуске системного приложения. Установка функции проверки подлинности в ЕОАК \_ disable \_ AAA позволяет приложению, работающему под привилегированной учетной записью (например, LocalSystem), предотвратить использование удостоверения для запуска ненадежных компонентов.

## <a name="related-topics"></a>Связанные темы

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

 

 
