---
description: Файл WiRunSQL.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: Выполнение инструкций SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650686"
---
# <a name="execute-sql-statements"></a>Выполнение инструкций SQL

Файл WiRunSQL.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). В этом примере показано, как использовать скрипт для выполнения SQL-запросов и обновлений в базе данных установщик Windows. Дополнительные сведения см. в статьях [синтаксис SQL](sql-syntax.md) и [примеры запросов к базе данных с помощью SQL и скрипта](examples-of-database-queries-using-sql-and-script.md).

Пример скрипта демонстрирует:

-   [**Метод опендатабасе (объект установщика)**](installer-opendatabase.md) и [**метод ластерроррекорд**](installer-lasterrorrecord.md) [**объекта установщика**](installer-object.md)
-   [**Метод OpenView**](database-openview.md)и [**метод Commit**](database-commit.md) [**объекта Database**](database-object.md)
-   [**Метод Execute**](view-execute.md) [ **объекта View**](view-object.md)
-   [**Свойство StringData**](record-stringdata.md) Пропертйоф [ **объекта Record**](record-object.md)

Для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows. Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис. Если первый аргумент имеет значение/?, отображается справка. или, если указано слишком мало аргументов. Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] . Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.

**cscript WiRunSQL.vbs \[ путь к \] \[ запросам SQL базы данных\]**

Укажите путь к установщик Windows базе данных. Укажите запросы SQL, которые должны выполняться. Обратите внимание, что запрос SQL должен быть заключен в двойные кавычки. Запросы SELECT отображают строки списка результатов, указанного в запросе. Столбцы двоичных данных, выбранные запросом, не отображаются.

Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md). Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).

Дополнительные сведения см. в статьях [Работа с запросами](working-with-queries.md) и [примеры запросов к базе данных с помощью SQL и скрипта](examples-of-database-queries-using-sql-and-script.md). Пример [локализации](a-localization-example.md) ДЕМОНСТРИРУЕТ использование SQL для [локализации столбцов базы данных](localizing-database-columns.md) и [обновления потока сводных данных](updating-a-summary-information-stream.md).

 

 



