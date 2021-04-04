---
description: Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 4.5 и более ранних версий.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Не поддерживается в установщик Windows 4,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811813"
---
# <a name="not-supported-in-windows-installer-45"></a>Не поддерживается в установщик Windows 4,5

Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 4,5 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. Чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. Сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Установщик Windows 4,5 доступна в качестве распространяемого пакета для Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1), Windows XP с пакетом обновления 2 (SP2) и более поздних версий и Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий. Полный список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

Следующие функции не поддерживаются в установщик Windows 4,5 и более ранних версиях.

[Стандартные действия](standard-actions.md)

-   [мсиконфигуресервицес](msiconfigureservices-action.md)

[Функции установщика](installer-functions.md)

-   [**мсиенумкомпонентсекс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**мсиенумклиентсекс**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**мсижеткомпонентпасекс**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Типы данных столбцов](column-data-types.md)

-   [**форматтедсддлтекст**](formattedsddltext.md)

[Свойства](properties.md)

-   [**мсифастинсталл**](msifastinstall.md)
-   [**мсиинсталлперусер**](msiinstallperuser.md)

[Таблицы базы данных](database-tables.md)

-   [Таблица Мсисервицеконфиг](msiserviceconfig-table.md)
-   [Таблица Мсисервицеконфигфаилуреактионс](msiserviceconfigfailureactions-table.md)
-   [Таблица Мсишорткутпроперти](msishortcutproperty-table.md)
-   [Таблица Мсилоккпермиссионсекс](msilockpermissionsex-table.md)

[контролевентс](control-events.md)

-   [Мсипринт таблице ControlEvent событие](msiprint-controlevent.md)
-   [Мсилаунчапп таблице ControlEvent событие](msilaunchapp-controlevent.md)

[Элементы управления](controls.md)

-   [Элемент управления HyperLink](hyperlink-control.md)
-   Поддержка [элементов управления "точечный рисунок](bitmap-control.md) " форматов файлов изображений WIC

[Внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Интерфейс автоматизации](automation-interface.md)

-   Свойства [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Клиентсекс**](installer-clientsex.md)
    -   [**Установщик. Компонентсекс**](installer-componentsex.md)
    -   [**Установщик. Компонентпасекс**](installer-componentpathex.md)

-   Свойства [ **объекта Component**](components.md)

    -   [**Component. Компоненткоде**](component-componentcode.md)
    -   [**Компонент. о. о. о.**](component-usersid.md)
    -   [**Component. Context**](component-context.md)

-   Свойства [ **клиентского объекта**](client.md)

    -   [**Клиент. ProductCode**](client-productcode.md)
    -   [**Client. Компоненткоде**](client-componentcode.md)
    -   [**Client., то есть**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Свойства объекта [**компонентинфо**](componentinfo.md)

    -   [**Компонентинфо. Компоненткоде**](componentinfo-componentcode.md)
    -   [**Компонентинфо. путь**](componentinfo-path.md)
    -   [**Компонентинфо. штат**](componentinfo-state.md)

## <a name="notes"></a>Примечания

Установщик Windows 4,5 не поддерживает некоторые функции, которые позволяют установить один пакет установки в контексте установки на компьютере или на уровне пользователя. Дополнительные сведения см. в разделе [Создание отдельного пакета](single-package-authoring.md).

Установщик Windows 4,5 не поддерживает некоторые параметры конфигурации служб, позволяющие пакету настраивать [службы](../services/services.md) на компьютере. Дополнительные сведения см. [в разделе Использование конфигурации служб](using-services-configuration.md).

Установщик Windows 4,5 не поддерживает некоторые функции, которые позволяют установщик Windows защищать новые учетные записи, [службы](../services/services.md)Windows, файлы, папки и разделы реестра. Дополнительные сведения см. в разделе [Защита ресурсов](securing-resources-.md).

Установщик Windows 4,5 не поддерживает некоторые функции, которые позволяют установить перечисление всех компонентов, установленных на компьютере, и получить путь к разделу для компонента. Дополнительные сведения см. в разделе [перечисление компонентов](enumerating-components-.md).

 

 
