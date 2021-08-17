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
ms.openlocfilehash: ac36bd89979d6cf0de0a4d574a47a6ce7060f90e5577402eba77aa2de42bbedb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131185"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> </dl>

 

 



