---
description: файл WiLstScr.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. в этом примере скрипта демонстрируется средство просмотра скриптов установщик Windows.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Просмотреть скрипт установщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d73c4c90266b94a02b9d73657fb95de75e153617ef1e34797f28035ee701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803985"
---
# <a name="view-installer-script"></a>Просмотреть скрипт установщика

файл WiLstScr.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). в этом примере скрипта демонстрируется средство просмотра скриптов установщик Windows.

В примере демонстрируется использование:

-   [**Метод Опендатабасе (объект установщика)**](installer-opendatabase.md)
-   Метод [**ластерроррекорд**](installer-lasterrorrecord.md) объекта [**Installer**](installer-object.md)
-   Метод [**OpenView**](database-openview.md) объекта [**Database**](database-object.md)
-   Метод [**Fetch**](view-fetch.md) объекта [**View**](view-object.md)
-   Метод [**форматтекст**](record-formattext.md)
-   [**FieldCount**](record-fieldcount.md) , свойство
-   Свойство [**StringData**](record-stringdata.md) объекта [**Record**](record-object.md)
-   [\_Таблица переformview](-transformview-table.md)

для использования этого примера требуется CScript.exe версия сервера скриптов Windows. Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис. Если первый аргумент имеет значение/?, отображается справка. или, если указано слишком мало аргументов. Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] . Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.

**cscript WiLstScr.vbs** *\[ путь к установщик Windows скрипту \] выполнения*

Укажите путь к скрипту выполнения установщика.

дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md). примеры служебных программ, не требующих Windows сервера сценариев, см. в разделе [средства разработки установщик Windows](windows-installer-development-tools.md).

 

 



