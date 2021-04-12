---
description: 'Сочетание пути, спецификации файла и флага рекурсии (Всзпас, Всзфилеспек и Брекурсиве соответственно) должны соответствовать одному из наборов файлов, добавленных в один из компонентов модуля записи с помощью Ивсскреатевритерметадата:: Аддфилестофилеграуп, Ивсскреатевритерметадата:: AddDatabaseFiles или IVssCreateWriterMetadata:: AddDatabaseLogFiles, если:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Семантические изменения в Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264021"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Семантические изменения в Windows Server 2003

Сочетание пути, спецификации файла и флага рекурсии (*всзпас*, *всзфилеспек* и *брекурсиве* соответственно) должны соответствовать одному из наборов файлов, добавленных в один из компонентов модуля записи с помощью [**ивсскреатевритерметадата:: Аддфилестофилеграуп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ивсскреатевритерметадата:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)или [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) , если:

-   Инициатор запроса добавляет новый целевой объект с помощью [**ивссбаккупкомпонентс:: аддневтаржет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).
-   Модуль записи добавляет сопоставление альтернативного расположения с помощью [**ивсскреатевритерметадата:: аддалтернателокатионмаппинг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   Существующие файлы добавляются в виде различных файлов с помощью [**ивсскомпонент:: адддифференцедфилесбиластмодифитиме**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Инициатор запроса указывает, что для восстановления набора файлов с помощью [**ивссбаккупкомпонентс:: аддалтернативелокатионмаппинг**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)использовалось сопоставление альтернативного расположения.

 

 



