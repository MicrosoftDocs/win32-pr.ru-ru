---
description: Установщик Windows можете оптимизировать исправления, чтобы сократить время, необходимое для применения исправлений к установленным приложениям.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Оптимизация исправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898846"
---
# <a name="patch-optimization"></a>Оптимизация исправления

Установщик Windows можете оптимизировать исправления, чтобы сократить время, необходимое для применения исправлений к установленным приложениям.

**Установщик Windows 2,0:** Не поддерживается. Для версий установщик Windows, выпущенных до установщик Windows 3,0, установка исправлений запускает полное восстановление приложения, что может занять значительно больше времени.

**Установщик Windows 3,0 и более поздних версий:** Процесс исправления изменяет только те части приложения, которые были изменены с помощью исправления.

**Установщик Windows 3,1 и более поздних версий:** Начиная с установщик Windows 3,1, оптимизация исправления требует, чтобы для всех исправлений в транзакции свойство Оптимизединсталлмоде было установлено в 1 (одно) в [таблице мсипатчметадата](msipatchmetadata-table.md).

Если исправление изменяет только следующие таблицы, установщик Windows 3,0 или более поздней версии пропускает действия, связанные со всеми другими таблицами, даже если эти действия перечислены в таблицах последовательности исходного пакета установки приложения (MSI-файла).

-   [админексекутесекуенце](adminexecutesequence-table.md)
-   [админуисекуенце](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [Файл](file-table.md)
-   [филесфпкаталог](filesfpcatalog-table.md)
-   [инсталлексекутесекуенце](installexecutesequence-table.md)
-   [инсталлуисекуенце](installuisequence-table.md)
-   [Носитель](media-table.md)
-   [MoveFile](movefile-table.md)
-   [мсиассембли](msiassembly-table.md)
-   [мсидигиталцертификате](msidigitalcertificate-table.md)
-   [мсидигиталсигнатуре](msidigitalsignature-table.md)
-   [мсифилехаш](msifilehash-table.md)
-   [мсипатчхеадерс](msipatchheaders-table.md)
-   [Обновление](patch-table.md)
-   [патчпаккаже](patchpackage-table.md)
-   [Свойство](property-table.md)
-   [Реестр](registry-table.md)
-   [сфпкаталог](sfpcatalog-table.md)
-   [Экспорт Typelib](typelib-table.md)
-   [\_Столбце](-columns-table.md)
-   [\_Хранилищах](-storages-table.md)
-   [\_Потоки](-streams-table.md)
-   [\_Таблицы](-tables-table.md)
-   [\_Таблица переformview](-transformview-table.md)
-   [\_Проверка](-validation-table.md)

Чтобы отключить параметр оптимизации исправлений, используйте политику [дисаблефливеигхтпатчинг](disableflyweightpatching.md) .

 

 



