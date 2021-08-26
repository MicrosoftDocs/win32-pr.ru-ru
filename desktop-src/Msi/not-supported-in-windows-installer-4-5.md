---
description: установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 4.5 и более ранних версий.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: не поддерживается в установщик Windows 4,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a285094610f0a00a39a26bb2d0683cb41afdfa3ed126ac27f7655c3cd56df17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979354"
---
# <a name="not-supported-in-windows-installer-45"></a>не поддерживается в установщик Windows 4,5

установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 4,5 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Windows установщик 4,5 доступен в качестве распространяемого пакета для Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1), Windows XP с пакетом обновления 2 (sp2) и более поздних версий и Windows Server 2003 с пакетом обновления 1 (sp1) и более поздних версий. полный список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

следующие функции не поддерживаются в установщик Windows 4,5 и более ранних версиях.

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

Windows Установщик 4,5 не поддерживает некоторые функции, которые позволяют установить один пакет установки в контексте установки на компьютере или на уровне пользователя. Дополнительные сведения см. в разделе [Создание отдельного пакета](single-package-authoring.md).

Windows Установщик 4,5 не поддерживает некоторые параметры конфигурации служб, позволяющие пакету настраивать [службы](../services/services.md) на компьютере. Дополнительные сведения см. [в разделе Использование конфигурации служб](using-services-configuration.md).

Windows установщик 4,5 не поддерживает некоторые функции, которые позволяют установщик Windows защищать новые учетные записи, Windows [службы](../services/services.md), файлы, папки и разделы реестра. Дополнительные сведения см. в разделе [Защита ресурсов](securing-resources-.md).

Windows Установщик 4,5 не поддерживает некоторые функции, которые позволяют установить перечисление всех компонентов, установленных на компьютере, и получить путь к разделу для компонента. Дополнительные сведения см. в разделе [перечисление компонентов](enumerating-components-.md).

 

 
