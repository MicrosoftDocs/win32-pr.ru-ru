---
description: Windows Установщик может оптимизировать исправления, чтобы сократить время, необходимое для применения исправлений к установленным приложениям.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Оптимизация исправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee37ba48764f6249410a6dfc2512245aa6ca6dfca68cff09ec15e06a42f9156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627647"
---
# <a name="patch-optimization"></a>Оптимизация исправления

Windows Установщик может оптимизировать исправления, чтобы сократить время, необходимое для применения исправлений к установленным приложениям.

**установщик Windows 2,0:** Не поддерживается. для версий установщик Windows, выпущенных до установщик Windows 3,0, установка исправлений запускает полное восстановление приложения, что может занять значительно больше времени.

**установщик Windows 3,0 и более поздних версий:** Процесс исправления изменяет только те части приложения, которые были изменены с помощью исправления.

**установщик Windows 3,1 и более поздних версий:** начиная с установщик Windows 3,1, оптимизация исправления требует, чтобы для всех исправлений в транзакции свойство оптимизединсталлмоде было установлено в 1 (одно) в [таблице мсипатчметадата](msipatchmetadata-table.md).

если исправление изменяет только следующие таблицы, установщик Windows 3,0 или более поздней версии пропускает действия, связанные со всеми другими таблицами, даже если эти действия перечислены в таблицах последовательности исходного пакета установки приложения (.msi файл).

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
-   [\_Столбцы](-columns-table.md)
-   [\_Хранилищах](-storages-table.md)
-   [\_Потоки](-streams-table.md)
-   [\_Таблицы](-tables-table.md)
-   [\_Таблица переformview](-transformview-table.md)
-   [\_Проверка](-validation-table.md)

Чтобы отключить параметр оптимизации исправлений, используйте политику [дисаблефливеигхтпатчинг](disableflyweightpatching.md) .

 

 



