---
description: Файл WiDiffDb.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. Этот пример скрипта создает временный файл преобразования между двумя установщик Windowsными базами данных и отображает преобразование.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Просмотр различий между двумя базами данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541191"
---
# <a name="view-differences-between-two-databases"></a>Просмотр различий между двумя базами данных

Файл WiDiffDb.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). Этот пример скрипта создает временный файл преобразования между двумя установщик Windowsными базами данных и отображает преобразование.

В примере демонстрируется использование:

-   [**Метод Опендатабасе (объект установщика)**](installer-opendatabase.md)
-   [**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)
-   [**Метод OpenView**](database-openview.md)
-   [**Свойство SummaryInformation (объект Database)**](database-summaryinformation.md)
-   [**Метод GenerateTransform**](database-generatetransform.md)
-   [**Метод Апплитрансформ**](database-applytransform.md)
-   [**Объект базы данных**](database-object.md)
-   [**Метод Fetch**](view-fetch.md) [ **объекта View**](view-object.md)
-   [**Свойство IsNull**](record-isnull.md)
-   [**Свойство StringData**](record-stringdata.md) [ **объекта Record**](record-object.md)
-   [\_Таблица переformview](-transformview-table.md)

Для использования этого примера требуется CScript.exe версия сервера сценариев Windows. Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис. Если первый аргумент имеет значение/?, отображается справка. или, если указано слишком мало аргументов. Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] . Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.

**cscript WiDiffDb.vbs** *\[ путь к исходному пути базы данных \] \[ к \] измененной базе данных*

Укажите путь к исходной базе данных установщик Windows. Укажите путь к измененной базе данных. В примере скрипта будет отображаться преобразование.

Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md). Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).

 

 



