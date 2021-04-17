---
description: Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 3.1 и более ранних версий.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: Не поддерживается в установщик Windows 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a221d80f56c5737cc5ae92a040a005ae42449e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674335"
---
# <a name="not-supported-in-windows-installer-31"></a>Не поддерживается в установщик Windows 3,1

Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 3,1 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. Чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. Сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Установщик Windows 3,1 доступна для Windows Server 2003, Windows XP или Windows 2000. Список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

Следующие функции не поддерживаются в установщик Windows 3,1 и более ранних версиях.

[Функции установщика](installer-functions.md)

-   [**мсижетпатчфилелист**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[Свойства](properties.md)

-   [**мсиарпсеттингсидентифиер**](msiarpsettingsidentifier.md)
-   [**мсидеплойменткомплиант**](msideploymentcompliant.md)
-   [**мсидисаблермрестарт**](msidisablermrestart.md)
-   [**мсилогфилелокатион**](msilogfilelocation.md)
-   [**мсилоггинг**](msilogging.md)
-   [**мсирестартманажерконтрол**](msirestartmanagercontrol.md)
-   [**мсирестартманажерсессионкэй**](msirestartmanagersessionkey.md)
-   [**мсирмшутдовн**](msirmshutdown.md)
-   [**мсируннинжелеватед**](msirunningelevated-.md)
-   [**мсисистемребутпендинг**](msisystemrebootpending.md)
-   [**мситаблетпк**](msitabletpc.md)
-   [**мсиусереаладминдетектион**](msiuserealadmindetection.md)

[Свойства сводных данных](summary-information-stream-reference.md)

-   [**Свойство "Сводка слов**](word-count-summary.md) " содержит новые биты флага, чтобы указать, требуются ли для установки пакета повышенные привилегии.

[Системная политика](system-policy.md)

-   [дисаблеаутоматикаппликатионшутдовн](disableautomaticapplicationshutdown.md)
-   [дисаблелоггингфромпаккаже](disableloggingfrompackage.md)

[Таблицы базы данных](database-tables.md)

-   [Таблица ярлыков](shortcut-table.md)

    Новые столбцы: Дисплайресаурцедлл, Дисплайресаурцеид, Дескриптионресаурцедлл и Дескриптионресаурцеид

[Диалоговые окна](dialog-boxes.md)

-   [Диалоговое окно Мсирмфилесинусе](msirmfilesinuse-dialog.md)

[Атрибуты элемента управления](control-attributes.md)

-   [елеватионшиелд](elevationshield-attribute.md)

[контролевентс](control-events.md)

-   [рмшутдовнандрестарт](rmshutdownandrestart-controlevent.md)

[Типы сообщений внешнего пользовательского интерфейса](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   ИНСТАЛЛЛОГМОДЕ \_ рмфилесинусе

[Установщик Windows в 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md)

-   атрибут **мсидбкомпонентаттрибутесдисаблерегистрирефлектион** в [таблице Component](component-table.md)

[Интерфейс автоматизации](automation-interface.md)

-   Методы [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Адвертисепродукт**](installer-advertiseproduct.md)
    -   [**Установщик. Адвертисескрипт**](installer-advertisescript.md)
    -   [**Установщик. Креатеадвертисескрипт**](installer-createadvertisescript.md)
    -   [**Установщик. Провидеассембли**](installer-provideassembly.md)

-   Свойства [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Патчфилес**](installer-patchfiles.md)
    -   [**Установщик. Продуктелеватед**](installer-productelevated.md)
    -   [**Установщик. Продуктинфофромскрипт**](installer-productinfofromscript.md)

## <a name="notes"></a>Примечания

Служба установщик Windows должна работать в Windows Vista, чтобы обеспечить возможность использования [диспетчера перезапуска](../rstmgr/restart-manager-portal.md), [*контроля учетных записей*](u-gly.md)и [исправлений контроля учетных записей (UAC)](user-account-control--uac--patching.md). Дополнительные сведения см. в статьях [использование установщик Windows с диспетчером перезапуска](using-windows-installer-with-restart-manager.md) и [Использование установщик Windows с контрольными записями контроля](using-windows-installer-with-uac.md) [учетных](user-account-control--uac--patching.md)записей.

Установщик Windows 3,1 поддерживает защиту файлов Windows (WFP) и не поддерживает защита ресурсов Windows (WRP). WRP в Windows Server 2008 и Windows Vista заменяет WFP в Windows Server 2003, Windows XP и Windows 2000. Сведения о установщик Windows и WFP см. [в разделе использование установщик Windows и защита ресурсов Windows](windows-resource-protection-on-windows-vista.md).

 

 
