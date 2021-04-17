---
description: В стандартном модуле слияния требуются следующие таблицы.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Таблицы базы данных модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674157"
---
# <a name="merge-module-database-tables"></a>Таблицы базы данных модуля слияния

В стандартном модуле слияния требуются следующие таблицы.



| Имя таблицы                                       | Комментировать                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Компонент](component-table.md)                 | НЕОБХОДИМОСТИ                                                                                       |
| [Каталог](directory-table.md)                 | НЕОБХОДИМОСТИ                                                                                       |
| [феатурекомпонентс](featurecomponents-table.md) | НЕОБХОДИМОСТИ                                                                                       |
| [Файл](file-table.md)                           | НЕОБХОДИМОСТИ                                                                                       |
| [ModuleSignature](modulesignature-table.md)     | НЕОБХОДИМОСТИ Слияние с базой данных установщика. Содержит сведения, идентифицирующие модуль слияния. |
| [модулекомпонентс](modulecomponents-table.md)   | НЕОБХОДИМОСТИ Слияние с базой данных установщика. Список всех компонентов в модуле слияния.     |



 

Следующие таблицы происходят только в модулях слияния или в других базах данных установщика, которые уже объединены с модулем слияния.



| Имя таблицы                                     | Комментировать                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [модуледепенденци](moduledependency-table.md) | Слияние с базой данных установщика. Список других модулей слияния, необходимых для этого модуля слияния.                |
| [модуликсклусион](moduleexclusion-table.md)   | Слияние с базой данных установщика. Список других модулей слияния, несовместимых с этим модулем слияния. |



 

Следующие таблицы Модулесекуенце встречаются только в модулях слияния.



| Имя таблицы                                                             | Комментировать                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [модулеадминуисекуенце](moduleadminuisequence-table.md)               | Выполняет слияние действий в [таблицу админуисекуенце](adminuisequence-table.md).               |
| [модулеадминексекутесекуенце](moduleadminexecutesequence-table.md)     | Выполняет слияние действий в [таблицу админексекутесекуенце](adminexecutesequence-table.md).     |
| [модулеадвтуисекуенце](moduleadvtuisequence-table.md)                 | Не используйте эту таблицу. Дополнительные сведения см. в разделе [адвтуисекуенце Table](advtuisequence-table.md). |
| [модулеадвтексекутесекуенце](moduleadvtexecutesequence-table.md)       | Выполняет слияние действий в [таблицу адвтексекутесекуенце](advtexecutesequence-table.md).       |
| [модулеигноретабле](moduleignoretable-table.md)                       | Содержит список таблиц в модуле, которые не объединены в MSI файл.                        |
| [модулеинсталлуисекуенце](moduleinstalluisequence-table.md)           | Выполняет слияние действий в [таблицу инсталлуисекуенце](installuisequence-table.md).           |
| [модулеинсталлексекутесекуенце](moduleinstallexecutesequence-table.md) | Выполняет слияние действий в [таблицу инсталлексекутесекуенце](installexecutesequence-table.md). |



 

В каждом настраиваемом модуле слияния необходимы следующие таблицы. Для создания настраиваемого модуля слияния требуется Mergemod.dll 2,0 или более поздней версии. Дополнительные сведения см. в разделе [настраиваемые модули слияния](configurable-merge-modules.md).



| Имя таблицы                                                 | Комментировать                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Таблица Модулесубститутион](modulesubstitution-table.md)   | НЕОБХОДИМОСТИ Эта таблица не объединяется с целевой базой данных установки. Задает настраиваемые поля в целевой базе данных и предоставляет шаблон для конфигурации каждого поля. |
| [Таблица Модулеконфигуратион](moduleconfiguration-table.md) | НЕОБХОДИМОСТИ Эта таблица не объединяется с целевой базой данных установки. Определяет настраиваемые атрибуты модуля.                                                                 |



 

Следующие таблицы установщика не могут встречаться в стандартном модуле слияния.

-   [ббконтрол](bbcontrol-table.md)
-   [Печат](billboard-table.md)
-   [ккпсеарч](ccpsearch-table.md)
-   [Ошибка](error-table.md)
-   [Компонент](feature-table.md)
-   [Таблица Лаунчкондитион](launchcondition-table.md)
-   [Носитель](media-table.md)
-   [Обновление](patch-table.md)
-   [Обновление](upgrade-table.md)

Следующие таблицы установщика являются необязательными в модулях слияния.

-   [актионтекст](actiontext-table.md)
-   [админексекутесекуенце](adminexecutesequence-table.md)
-   [админуисекуенце](adminuisequence-table.md)
-   [адвтексекутесекуенце](advtexecutesequence-table.md)
-   [адвтуисекуенце](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [аппсеарч](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Класс](class-table.md)
-   [ComboBox](combobox-table.md)
-   [комплокатор](complocator-table.md)
-   [Управление](control-table.md)
-   [Таблица controlcondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Диалоговое окно](dialog-table.md)
-   [дрлокатор](drlocator-table.md)
-   [дупликатефиле](duplicatefile-table.md)
-   [Среда](environment-table.md)
-   [Таблица eventmapping](eventmapping-table.md)
-   [Расширение](extension-table.md)
-   [Шрифт](font-table.md)
-   [Значок](icon-table.md):
-   [инифиле](inifile-table.md)
-   [инилокатор](inilocator-table.md)
-   [инсталлексекутесекуенце](installexecutesequence-table.md)
-   [инсталлуисекуенце](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [MIME](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [одбкаттрибуте](odbcattribute-table.md)
-   [одбкдатасаурце](odbcdatasource-table.md)
-   [одбкдривер](odbcdriver-table.md)
-   [одбксаурцеаттрибуте](odbcsourceattribute-table.md)
-   [одбктранслатор](odbctranslator-table.md)
-   [Таблица ProgID](progid-table.md)
-   [Свойство](property-table.md)
-   [публишкомпонент](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Таблица реестра](registry-table.md)
-   [реглокатор](reglocator-table.md)
-   [ремовефиле](removefile-table.md)
-   [ремовеинифиле](removeinifile-table.md)
-   [ремоверегистри](removeregistry-table.md)
-   [ресервекост](reservecost-table.md)
-   [селфрег](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [сервицеинсталл](serviceinstall-table.md)
-   [Клавиша](shortcut-table.md)
-   [Образец](signature-table.md)
-   [Система создала шрифт](textstyle-table.md)
-   [Экспорт Typelib](typelib-table.md)
-   [уитекст](uitext-table.md)
-   [Команда](verb-table.md)

 

 



