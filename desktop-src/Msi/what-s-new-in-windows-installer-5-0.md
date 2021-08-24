---
description: сведения в этом разделе определяют дополнения и изменения, доступные в установщик Windows&\# 160; 5.0.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: новые возможности установщик Windows 5,0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: 82c6ae3bf5c6781ba84d18b366998c74deedd4ca0fa4c61ac452b1d0ec409850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145227"
---
# <a name="whats-new-in-windows-installer-50"></a>новые возможности установщик Windows 5,0

сведения в этом разделе определяют дополнения и изменения, доступные в установщик Windows 5,0.

Windows Установщик 5,0 входит в состав следующих версий Windows:

* клиент: Windows 7 и все более поздние версии.
* сервер: Windows server 2008 R2 и все более поздние версии.

> [!NOTE]
> распространяемый пакет для установщик Windows 5,0 не существует. список распространяемых пакетов, доступных для предыдущих версий установщик Windows, см. в разделе [установщик Windows распространяемые пакеты](windows-installer-redistributables.md). полный список установщик Windows версий см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

Эта страница представлена в качестве руководства по документации. Чтобы определить фактические требования к операционной системе, ознакомьтесь с разделом требования на основных страницах справочника. части установщик Windows, которые не связаны с этой страницей, могут быть доступны в другой версии установщик Windows. сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

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

[Свойства сводных данных](summary-information-stream-reference.md)

-   в [**сводке шаблона**](template-summary.md) есть новые значения, указывающие, что база данных совместима с Windows RT или платформой Arm64.

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

[Внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Интерфейс автоматизации](automation-interface.md)

-   Свойства [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Клиентсекс**](installer-clientsex.md)
    -   [**Установщик. Компонентсекс**](installer-componentsex.md)
    -   [**Установщик. Компонентпасекс**](installer-componentpathex.md)

-   Свойства [ **объекта Components**](components.md)

    -   [**Components. Компоненткоде**](component-componentcode.md)
    -   [**Компоненты. о. о. о.**](component-usersid.md)
    -   [**Components. Context**](component-context.md)

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

разработчики программы установки могут использовать установщик Windows 5,0 для создания одного пакета установки, поддерживающего установку на компьютере или установку приложения для отдельных пользователей. Дополнительные сведения см. в разделе [Создание отдельного пакета](single-package-authoring.md). Средство оценки внутренней согласованности [ICE105](ice-105.md) проверяет, что пакет был создан для установки в контексте для каждого пользователя. Приложение, которое может устанавливаться, обновляться, запускаться и удаляться обычным пользователем без повышения прав, называется Per-Userным приложением (PUA). PUA обеспечивает более удобный пользовательский интерфейс, уменьшает влияние на систему и других пользователей компьютера и резервирует контроль учетных записей в ситуациях, требующих повышения прав пользователя. возможности создания отдельных пакетов установщик Windows 5,0 могут упростить разработку Per-User приложений.

параметры конфигурации служб позволяют пакету установщик Windows настраивать [службы](../services/services.md) на компьютере. Дополнительные сведения см. [в разделе Использование конфигурации служб](using-services-configuration.md).

начиная с установщик Windows 5,0, пакет установщик Windows может защищать новые учетные записи, Windows [службы](../services/services.md), файлы, папки и разделы реестра. В таблице [мсилоккпермиссионсекс](msilockpermissionsex-table.md) можно указать дескриптор безопасности, который запрещает разрешения, задает наследование разрешений от родительского ресурса или указывает разрешения новой учетной записи. Дополнительные сведения см. в разделе [Защита ресурсов](securing-resources-.md).

Windows Установщик 5,0 может перечислить все компоненты, установленные на компьютере, и получить путь к разделу для компонента. Дополнительные сведения см. в разделе [перечисление компонентов](enumerating-components-.md).

Windows установщик 5,0, работающий на Windows Server 2012 или Windows 8, поддерживает установку утвержденных приложений на Windows RT. пакет установщик Windows, исправление или преобразование, которые не были подписаны корпорацией майкрософт, не могут быть установлены на Windows RT. Свойство [**Сводка шаблона**](template-summary.md) Указывает платформу, совместимую с базой данных установки, и должна включать значение для Windows RT.

Windows установщик 5,0, выполняющийся на Windows 10 процессорах Arm64, поддерживает установку приложений, скомпилированных специально для платформы Arm64.  Свойство [**Сводка шаблона**](template-summary.md) этих пакетов должно включать значение Arm64. 

 
