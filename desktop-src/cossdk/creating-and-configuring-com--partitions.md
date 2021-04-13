---
description: Администраторы могут использовать COM+ для программного создания и настройки разделов COM+.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Создание и Настройка разделов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538822"
---
# <a name="creating-and-configuring-com-partitions"></a>Создание и Настройка разделов COM+

Администраторы могут использовать COM+ для программного создания и настройки разделов COM+. На самом деле, все задачи создания и настройки, которые администратор может выполнять из служб компонентов или Active Directory средства администрирования пользователей и компьютеров, можно выполнять с помощью коллекций COM+, объектов и интерфейсов, а также с помощью интерфейса системы Active Directory (ADSI).

**Windows XP:** Возможность создания, настройки или делегирования разделов COM+ недоступна. Глобальный раздел является единственным доступным разделом COM+.

* * Windows 2000: * * служба разделов COM+ недоступна в Windows 2000.

> [!Note]  
> Служба "разделы COM+" не включена по умолчанию. Чтобы использовать службу "разделы COM+", необходимо включить ее с помощью средства администрирования служб компонентов или путем изменения свойства Партитионсенаблед в коллекции [**локалкомпутер**](localcomputer.md) на true.

 

Для выполнения задач, связанных с секциями, COM+ предоставляет следующие программные элементы:

-   Методы и свойства интерфейса [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) в классе [**комадминкаталог**](comadmincatalog.md) :
    -   Свойство [**куррентпартитион**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .
    -   Свойство [**куррентпартитионид**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .
    -   Свойство [**куррентпартитионнаме**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .
    -   Метод [**флушпартитионкаче**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .
    -   Метод [**жетпартитионид**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .
    -   Метод [**жетпартитионнаме**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .
    -   Свойство [**глобалпартитионид**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .
-   Набор объектов COM+ для создания секций и управления ими в Active Directory.
-   Раздел реестра COM+, **партитионкаче**, для изменения размера кэша раздела.
-   Набор связанных с секциями [коллекций администрирования com+](com--administration-collections.md):
    -   Коллекция [**partitions**](partitions.md) .
    -   Коллекция [**партитионусерс**](partitionusers.md) .
    -   Коллекция [**ролесфорпартитион**](rolesforpartition.md) .
    -   Коллекция [**усерсинпартитионроле**](usersinpartitionrole.md) .
-   Свойства других [коллекций администрирования com+](com--administration-collections.md):
    -   Свойство PartitionID в коллекции [**аппликатионинстанцес**](applicationinstances.md) .
    -   Свойство Апппартитионид коллекции [**приложений**](applications.md) .
    -   Свойства Партитиондескриптион, PartitionID и PartitionName в коллекции [**филесфоримпорт**](filesforimport.md) .
    -   Свойства Дспартитионлукупенаблед, Локалпартитионлукупенаблед и Партитионсенаблед коллекции [**локалкомпутер**](localcomputer.md) .
    -   Свойства Евенткласспартитионид и Субскриберпартитионид в коллекции [**субскриптионсфоркомпонент**](subscriptionsforcomponent.md) .
    -   Свойства Евенткласспартитионид и Субскриберпартитионид в коллекции [**трансиентсубскриптионс**](transientsubscriptions.md) .

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
</dt> <dt>

[Установка прав администратора для секции](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



