---
description: API скриптов для WMI Reference описывает каждый объект скрипта с использованием определенного синтаксиса. Описание этого синтаксиса см. в разделе соглашения о документе для API скриптов.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Создание скриптов для объектов API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263809"
---
# <a name="scripting-api-objects"></a>Создание скриптов для объектов API

API скриптов для WMI Reference описывает каждый объект скрипта с использованием определенного синтаксиса. Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

В следующей таблице перечислены объекты сценариев WMI и их использование.



| Объект                                               | Описание                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Конструирует и анализирует значения даты и [времени](date-and-time-format.md) CIM.                                                                                                                                                                                 |
| [**свбемевентсаурце**](swbemeventsource.md)         | Получает события в сочетании с [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**свбемластеррор**](swbemlasterror.md)             | Предоставляет расширенные сведения об ошибке при возникновении ошибки.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Получает объект [**SwbemServices**](swbemservices.md) , который может получить доступ к инструментарию WMI на определенном компьютере узла.                                                                                                                                     |
| [**свбеммесод**](swbemmethod.md)                   | Содержит одно определение метода WMI.                                                                                                                                                                                                               |
| [**свбеммесодсет**](swbemmethodset.md)             | Возвращает коллекцию объектов [**свбеммесод**](swbemmethod.md) .                                                                                                                                                                                       |
| [**свбемнамедвалуе**](swbemnamedvalue.md)           | Содержит одно именованное значение.                                                                                                                                                                                                                         |
| [**свбемнамедвалуесет**](swbemnamedvalueset.md)     | Получает доступ к коллекции объектов [**свбемнамедвалуе**](swbemnamedvalue.md) .                                                                                                                                                                     |
| [**SWbemObject**](swbemobject.md)                   | Содержит и манипулирует одним классом объекта WMI или экземпляром.                                                                                                                                                                                        |
| [**свбемобжектекс**](swbemobjectex.md)               | Расширяет функциональные возможности [**SWbemObject**](swbemobject.md). Этот объект добавляет метод [**Refresh**](swbemrefresher-refresh.md) для объектов [**свбемрефрешер**](swbemrefresher.md) .                                                           |
| [**свбемобжектпас**](swbemobjectpath.md)           | Создает и проверяет путь к объекту.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Получает доступ к коллекции объектов [**SWbemObject**](swbemobject.md) .                                                                                                                                                                             |
| [**свбемпривилеже**](swbemprivilege.md)             | Задает или очищает привилегию.                                                                                                                                                                                                                            |
| [**свбемпривилежесет**](swbemprivilegeset.md)       | Получает доступ к коллекции объектов [**свбемпривилеже**](swbemprivilege.md) .                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Содержит одно свойство WMI.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Получает доступ к коллекции объектов [**SWbemProperty**](swbemproperty.md) .                                                                                                                                                                         |
| [**свбемкуалифиер**](swbemqualifier.md)             | Содержит квалификатор одного свойства.                                                                                                                                                                                                                  |
| [**свбемкуалифиерсет**](swbemqualifierset.md)       | Получает доступ к коллекции объектов [**свбемкуалифиер**](swbemqualifier.md) .                                                                                                                                                                       |
| [**свбемрефрешер**](swbemrefresher.md)             | Собирает и обновляет значения свойств объекта за одну операцию.                                                                                                                                                                                          |
| [**свбемрефрешаблеитем**](swbemrefreshableitem.md) | Представляет один обновляемый элемент в объекте [**свбемрефрешер**](swbemrefresher.md) , например свойство.                                                                                                                                     |
| [**свбемсекурити**](swbemsecurity.md)               | Управляет параметрами безопасности, такими как [**привилегии**](swbemsecurity-privileges.md)модели COM, [**аусентикатионлевел**](swbemsecurity-authenticationlevel.md)и [**имперсонатионлевел**](swbemsecurity-impersonationlevel.md).   |
| [**SWbemServices**](swbemservices.md)               | Создает, обновляет и извлекает экземпляры или классы.                                                                                                                                                                                                  |
| [**свбемсервицесекс**](swbemservicesex.md)           | Расширяет функциональные возможности [**SwbemServices**](swbemservices.md). Этот объект добавляет методы [**размещения**](swbemservicesex-put.md) и [**путасинк**](swbemservicesex-putasync.md) , чтобы разрешить сохранение класса или экземпляра в нескольких пространствах имен. |
| [**свбемсинк**](swbemsink.md)                       | Получает результаты асинхронных операций и уведомлений о событиях, используемых клиентскими приложениями.                                                                                                                                        |



 

 

 



