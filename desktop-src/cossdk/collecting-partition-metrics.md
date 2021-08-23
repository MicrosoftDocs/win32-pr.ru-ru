---
description: Сбор метрик секции
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Сбор метрик секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8168972a0bac0b4eb79c5adde3530d1a0673469adff6b66b4c1b31cc6446bca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047691"
---
# <a name="collecting-partition-metrics"></a>Сбор метрик секции

В некоторых случаях Организация может захотеть собираются сведения об использовании приложения COM+ в целях мониторинга, планирования загрузки и учета ресурсов.

Например, поставщику службы приложений (ASP) может потребоваться начисление клиента на использование ресурсов. Для этого COM+ позволяет получать сведения о событиях и метриках на основе каждого раздела.

Чтобы получить эти сведения для определенной секции, необходимо указать для каждого интерфейса инструментария COM+ элемент идентификатора секции в стандартной структуре событий. Структура событий является первым значением интерфейса инструментария COM+. Дополнительные сведения см. в разделе [интерфейсы инструментария com+](com--instrumentation-interfaces.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка кэша секций](configuring-the-partition-cache.md)
</dt> <dt>

[Группирование приложений в секции](grouping-applications-into-partitions.md)
</dt> <dt>

[Управление локальными секциями](managing-local-partitions.md)
</dt> <dt>

[Управление секциями в Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Установка прав администратора для секции](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



