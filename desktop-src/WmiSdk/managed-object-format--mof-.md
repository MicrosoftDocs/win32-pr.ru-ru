---
description: MOF-файл (MOF) — это язык, используемый для описания классов модель CIM (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF-файл
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693446"
---
# <a name="managed-object-format-mof"></a>MOF-файл

MOF-файл (MOF) — это язык, используемый для описания классов [*модель CIM (CIM)*](gloss-c.md) .

Для поставщиков WMI рекомендуется реализовать новые классы WMI в MOF-файлах, компилируемых с помощью [**Mofcomp.exe**](mofcomp.md) в [*репозиторий WMI*](gloss-w.md). Кроме того, можно создавать классы и экземпляры CIM и управлять ими с помощью [API COM для WMI](com-api-for-wmi.md).

Поставщик WMI обычно состоит из MOF-файла, который определяет классы данных и событий, для которых поставщик возвращает данные, и DLL-файл, содержащий код, предоставляющий данные. Дополнительные сведения см. [в разделе Предоставление данных инструментарию WMI](providing-data-to-wmi.md).

Клиентские сценарии и приложения WMI могут запрашивать экземпляры классов MOF поставщика или подписываться на получение уведомлений о событиях.

С помощью MOF можно выполнять следующие задачи:

-   [Компиляция MOF-файлов](compiling-mof-files.md)
-   [Создание класса](creating-a-class.md)
-   [Создание экземпляра](creating-an-instance.md)
-   [Создание метода](creating-a-method.md)
-   [Добавление квалификатора](adding-a-qualifier.md)
-   [Создание комментария](creating-a-comment.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> </dl>

 

 



