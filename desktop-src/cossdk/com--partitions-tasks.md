---
description: Задачи секций COM+
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Задачи секций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262570"
---
# <a name="com-partitions-tasks"></a>Задачи секций COM+

В следующих подразделах этого раздела приводятся пошаговые инструкции по использованию разделов COM+.

**Windows XP:** Возможность создания, настройки или делегирования разделов COM+ недоступна. Глобальный раздел является единственным доступным разделом COM+.

* * Windows 2000: * * служба разделов COM+ недоступна в Windows 2000.



| Раздел                                                                                                         | Описание                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Создание и Настройка разделов COM+](creating-and-configuring-com--partitions.md)<br/>           | Описывает создание и настройку раздела COM+.<br/>                             |
| [Управление локальными секциями](managing-local-partitions.md)<br/>                                         | Описывает управление разделами COM+, которые не находятся в Active Directory.<br/>       |
| [Управление секциями в Active Directory](managing-partitions-within-active-directory.md)<br/>     | Описывает, как управлять разделами COM+, указанными в Active Directory.<br/> |
| [Установка прав администратора для секции](setting-administrative-rights-for-a-partition.md)<br/> | Описание настройки прав доступа для раздела COM+.<br/>                      |
| [Группирование приложений в секции](grouping-applications-into-partitions.md)<br/>                 | Описание настройки приложений COM+ для принадлежности к разделу COM+. <br/>        |
| [Сбор метрик секции](collecting-partition-metrics.md)<br/>                                   | Описывает, как выполнять получение данных о разделах COM+.<br/>                                |
| [Настройка кэша секций](configuring-the-partition-cache.md)<br/>                             | Описание настройки кэша разделов COM+.<br/>                                |



 

> [!Note]  
> Служба "разделы COM+" не включена по умолчанию. Чтобы использовать службу "разделы COM+", необходимо включить ее с помощью средства администрирования служб компонентов или путем изменения свойства Партитионсенаблед в коллекции [**локалкомпутер**](localcomputer.md) на true.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные понятия о разделах COM+](com--partitions-concepts.md)
</dt> </dl>

 

 




