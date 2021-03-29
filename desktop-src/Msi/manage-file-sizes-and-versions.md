---
description: Файл WiFilVer.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере показано, как можно использовать скрипт для создания отчетов или обновления версии файла, размера и сведений о языке.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Управление размерами и версиями файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810732"
---
# <a name="manage-file-sizes-and-versions"></a>Управление размерами и версиями файлов

Файл WiFilVer.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). В этом примере показано, как можно использовать скрипт для создания отчетов или обновления версии файла, размера и сведений о языке.

В этом примере также показаны установщик Windows действия, доступ к базе данных установщик Windows и использование следующих элементов:

-   Метод [**Installer. Опендатабасе**](installer-opendatabase.md) [ **объекта Installer**](installer-object.md)
-   Свойство [**Installer. FileAttributes**](installer-fileattributes.md)
-   Метод [**Installer. FileHash**](installer-filehash.md)
-   Метод [**Installer. FileVersion**](installer-fileversion.md)
-   Метод [**Installer. Ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)
-   [**Database. OpenView,**](database-openview.md) метод
-   Свойство [**Database. SummaryInformation**](database-summaryinformation.md) [ **объекта Database**](database-object.md)
-   [**Session. DoAction,**](session-doaction.md) метод
-   [**Session. Property**](session-session.md)
-   Свойство [**Session. SourcePath**](session-sourcepath.md)
-   Свойство [**Session. Mode**](session-mode.md) [ **объекта Session**](session-object.md)
-   Свойство [**Record. StringData**](record-stringdata.md)
-   Свойство [**Record. IntegerData**](record-integerdata.md) [ **объекта Record**](record-object.md)

Для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows. Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке с помощью следующего синтаксиса:

**cscript WiFilVer.vbs \[ путь к \] \[ необязательным исходным расположениям базы данных\]**

Также необходимо учитывать следующее:

-   Если первый аргумент имеет значение/?, отображается справка. или, если указано слишком мало аргументов.
-   Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .
-   Пример возвращает значение 0 (ноль) для успешного выполнения, 1 (один), если вызывается Справка, и 2 (два) в случае сбоя сценария.

Укажите установщик Windows базу данных, которую необходимо обновить, которая должна находиться в корне исходного файла. Однако можно указать источники базы данных в разных расположениях. Если источник сжат, все файлы открываются в корне.

Следующие параметры можно указать в любом расположении в командной строке.



| Параметр                | Описание                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *параметр не указан* | Отображает сведения о файле базы данных.                                            |
| /U                    | Обновите размер файла, версию и сведения о языке в базе данных источника. |



 

Дополнительные сведения см. в статьях [примеры сценариев установщик Windows](windows-installer-scripting-examples.md) и [средства разработки установщик Windows](windows-installer-development-tools.md).

 

 



