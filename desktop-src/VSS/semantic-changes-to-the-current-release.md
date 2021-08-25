---
description: 'Сочетание пути, спецификации файла и флага рекурсии (Всзпас, Всзфилеспек и Брекурсиве соответственно) должны соответствовать одному из наборов файлов, добавленных в один из компонентов модуля записи с помощью Ивсскреатевритерметадата:: Аддфилестофилеграуп, Ивсскреатевритерметадата:: AddDatabaseFiles или IVssCreateWriterMetadata:: AddDatabaseLogFiles, если:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: семантические изменения в Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8319259dc27c981822bb242d20243264ca9025d959693aafcb3836976fd7754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866264"
---
# <a name="semantic-changes-to-windows-server-2003"></a>семантические изменения в Windows Server 2003

Сочетание пути, спецификации файла и флага рекурсии (*всзпас*, *всзфилеспек* и *брекурсиве* соответственно) должны соответствовать одному из наборов файлов, добавленных в один из компонентов модуля записи с помощью [**ивсскреатевритерметадата:: Аддфилестофилеграуп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ивсскреатевритерметадата:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)или [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) , если:

-   Инициатор запроса добавляет новый целевой объект с помощью [**ивссбаккупкомпонентс:: аддневтаржет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).
-   Модуль записи добавляет сопоставление альтернативного расположения с помощью [**ивсскреатевритерметадата:: аддалтернателокатионмаппинг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   Существующие файлы добавляются в виде различных файлов с помощью [**ивсскомпонент:: адддифференцедфилесбиластмодифитиме**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Инициатор запроса указывает, что для восстановления набора файлов с помощью [**ивссбаккупкомпонентс:: аддалтернативелокатионмаппинг**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)использовалось сопоставление альтернативного расположения.

 

 



