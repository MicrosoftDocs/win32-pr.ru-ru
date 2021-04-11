---
description: Таблицы установщик Windows базы данных можно экспортировать в текстовые файлы ASCII с помощью Мсидатабасикспорт или метода Export объекта Database.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Файлы архивов текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910363"
---
# <a name="text-archive-files"></a>Файлы архивов текста

Таблицы установщик Windows базы данных можно экспортировать в текстовые файлы ASCII с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) или метода [**Export**](database-export.md) объекта [**Database**](database-object.md) . Сведения в этих файлах текстовых архивов затем можно импортировать обратно в базу данных установщик Windows с помощью [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) или метода [Import](database-import.md) объекта **Database** .

Такие средства, как [msidb.exe](msidb-exe.md) , способны экспортировать и импортировать текстовые архивные файлы. [Примеры сценариев установщик Windows](windows-installer-scripting-examples.md) , в которых можно экспортировать и импортировать текстовые архивные файлы из базы данных, см. в разделе [Экспорт файлов](export-files.md) и [Импорт файлов](import-files.md) .

> [!Note]  
> Файлы текстовых архивов не предназначены для изменения базы данных установки. Для создания и изменения пакета установки следует использовать средство редактирования таблиц установщик Windows, например [Orca](orca-exe.md) или сторонний инструмент.

 

Файлы архивов текста можно использовать в следующих целях.

-   Файлы архивов текста можно использовать с системами управления версиями.
-   Чтобы удалить неиспользуемое дисковое пространство и сократить окончательный размер MSI-файлов. См. раздел [уменьшение размера MSI файла](reducing-the-size-of-an--msi-file.md).
-   Для добавления сведений о локализации в базу данных установки. Дополнительные сведения см. в разделе [Обработка кодовых страниц импортированных и экспортированных таблиц](code-page-handling-of-imported-and-exported-tables.md).

-   Для определения кодовой страницы базы данных. См. раздел [Определение кодовой страницы базы данных установки](determining-an-installation-database-s-code-page.md).
-   Для задания кодовой страницы базы данных. См. раздел [Настройка кодовой страницы базы данных](setting-the-code-page-of-a-database.md).
-   Для увеличения предельного значения столбца базы данных. Экспортируйте таблицу с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), измените экспортированный файл IDT, а затем импортируйте таблицу с помощью [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Авторы не могут изменять типы данных столбцов, допустимость значений NULL или атрибуты локализации любых столбцов в стандартных таблицах. См. также [Создание большого пакета](authoring-a-large-package.md).

На следующих страницах описываются текстовые архивные страницы и их форматы.

-   [Формат файла архива](archive-file-format.md)
-   [Данные ASCII в текстовых архивных файлах](ascii-data-in-text-archive-files.md)
-   [\_форцекодепаже](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



