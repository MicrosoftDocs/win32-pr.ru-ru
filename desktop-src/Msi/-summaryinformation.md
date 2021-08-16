---
description: '\_Таблица SummaryInformation — это специальная таблица, используемая в потоке сводных данных. можно получить или задать поток сводных данных установщик Windows базы данных путем экспорта или импорта текстового файла архива с именем \_ SummaryInformation. idt.'
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3824ceb9b3ad12338d84dfeea016a3c7e4404c274543cc691dc6ea0fb121bd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805740"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

\_Таблица SummaryInformation — это специальная таблица, используемая в [потоке сводных данных](summary-information-stream.md). можно получить или задать поток сводных данных установщик Windows базы данных путем экспорта или импорта [текстового файла архива](text-archive-files.md) с именем \_ SummaryInformation. idt.

Файл IDT экспортированной \_ таблицы SummaryInformation имеет следующий формат.

-   Первая строка содержит имена столбцов таблицы, разделенные символами табуляции: PropertyId и value. Список свойств и их идентификаторов см. в разделе [Сводные сведения о наборе свойств потока](summary-information-stream-property-set.md) .
-   Вторая строка содержит определения столбцов, разделенные символами табуляции. Определения столбцов задаются так же, как и в стандартном [формате файлового архива](archive-file-format.md). IDT. Столбец PropertyId может быть коротким целым числом, не допускающим значения NULL. Столбец значения может быть локализованной строкой 255, не допускающей значения NULL.
-   Третья строка представляет собой имя таблицы и имя первичного ключевого столбца, разделенные вкладками: \_ SummaryInformation и PropertyId.
-   Остальные строки в файле представляют идентификатор процесса и связанное значение, разделенные символами табуляции. Дата и время в \_ SummaryInformation имеют формат: гггг/мм/дд чч:: мм:: СС. Например, 1999/03/22 15:25:45.

Ниже приведен пример [сводного информационного потока](summary-information-stream.md) базы данных в формате IDT.

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

При использовании [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) или метода [Import](database-import.md) объекта [**базы данных**](database-object.md) для импорта таблицы текстовых архивов с именем \_ SummaryInformation в базу данных установщика вы пишете поток "05SummaryInformation" в базу данных.

 

 



