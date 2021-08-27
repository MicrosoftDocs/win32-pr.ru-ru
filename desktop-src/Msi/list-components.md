---
description: файл WiCompon.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. этот пример скрипта можно использовать для перечисления компонентов в базе данных установщик Windows.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Составить список компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec396e66ed55d78131c74b85432b2f01829cdb5400fc5c00a6ced5725edadeae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129324"
---
# <a name="list-components"></a>Составить список компонентов

файл WiCompon.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). этот пример скрипта можно использовать для перечисления компонентов в базе данных установщик Windows.

В этом примере демонстрируется использование различных первичных ключей в [таблице Component](component-table.md).

В этом примере также демонстрируется:

-   Метод [**опендатабасе (объект установщика)**](installer-opendatabase.md), [**метод СоздатьЗапись**](installer-createrecord.md)и [**метод ластерроррекорд**](installer-lasterrorrecord.md) [**объекта установщика**](installer-object.md).
-   [**Метод OpenView**](database-openview.md), [**свойство Таблеперсистент**](database-tablepersistent.md)и [**свойство примарикэйс**](database-primarykeys.md) [**объекта Database**](database-object.md).
-   [**Метод Execute**](view-execute.md) и [**метод Fetch**](view-fetch.md) [**объекта View**](view-object.md).
-   Свойство [**Свойства StringData**](record-stringdata.md) [**объекта Record**](record-object.md).

для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows. Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис. Если первый аргумент имеет значение/?, отображается справка. или, если указано слишком мало аргументов. Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] . Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.

**cscript WiCompon.vbs \[ путь к \] \[ имени компонента базы данных\]**

укажите путь к базе данных установщик Windows. Укажите имя компонента. Имя должно быть указано в столбце Component [таблицы Component](component-table.md). Если имя компонента пропущено, будут перечислены все компоненты. Если в \* качестве имени компонента используется звездочка (), WiCompon.vbs отображает список всех компонентов. Обратите внимание, что большие базы данных лучше отображать с помощью CScript, а не WScript.

дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md). примеры служебных программ, не требующих Windows сервера сценариев, см. в разделе [средства разработки установщик Windows](windows-installer-development-tools.md).

 

 



