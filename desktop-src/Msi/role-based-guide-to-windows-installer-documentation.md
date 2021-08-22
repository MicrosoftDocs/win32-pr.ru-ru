---
description: Windows Установщик является рекомендуемым решением для установки и настройки приложений на Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: руководство на основе ролей для установщик Windows документации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625866"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>руководство на основе ролей для установщик Windows документации

Windows Установщик является рекомендуемым решением для установки и настройки приложений на Windows. Поэтому некоторые сведения, содержащиеся в этом пакете SDK, будут интересны для широкого спектра разработки программного обеспечения и ИТ-специалистов. Этот раздел представлен в качестве руководства для читателей, которые предпочитают просматривать ссылки на разделы, упорядоченные по сценариям Professional Role и Common Task. Поскольку роли могут сильно различаться в разных организациях, приведенная ниже группировка должна рассматриваться в качестве пути к расположению, чтобы начать поиск необходимой информации.

-   [Разработчики приложений](#application-developers)
-   [Авторы программы установки](#setup-authors)
-   [ИТ-специалисты](#it-professionals)
-   [Разработчики инфраструктуры](#infrastructure-developers)

эта документация предназначена для разработчиков программного обеспечения, которые хотят создавать приложения, использующие установщик Windows. В качестве основного источника справочных материалов по установщику пакет SDK предоставляет сведения о пакетах установки и службе установщика. Он содержит полные описания прикладного программного интерфейса (API) и элементов базы данных установщика.

дополнительные сведения см. в разделе [другие источники сведений о установщик Windows](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Разработчики приложений

разработчики приложений создают приложения, вызывающие установщик Windows программный интерфейс приложения и устанавливающие Windows пакеты установщика во время выполнения. установщик Windows может выполнять работу в таких приложениях, как самостоятельное восстановление и установка по запросу. Как правило, разработчики приложений выполняют следующие действия:

-   Включить установку по запросу приложений во время выполнения из другого приложения.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование функций установщика](using-installer-functions.md)
    -   [Справочник по функциям установщика](installer-function-reference.md)
    -   [Установка по запросу](installation-on-demand.md)
    -   [Управление компонентами](component-management.md)
    -   [Изменение ярлыков установщика](editing-installer-shortcuts.md)
    -   [**Олеадвтсуппорт, свойство**](oleadvtsupport.md)
    -   [Поддержка платформ объявления](platform-support-of-advertisement.md)

-   Включение самостоятельного восстановления приложений путем повторной установки компонентов при необходимости во время выполнения.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование функций установщика](using-installer-functions.md)
    -   [Справочник по функциям установщика](installer-function-reference.md)
    -   [Устойчивость](resiliency.md)
    -   [Отказоустойчивость источника](source-resiliency.md)
    -   [Поиск неработающей функции или компонента](searching-for-a-broken-feature-or-component.md)
    -   [Замена существующих файлов](replacing-existing-files.md)

-   Отображать пользовательский интерфейс для получения сведений о пользователях и предпочтениях конфигурации при первом установке или запуске приложения. пользовательский интерфейс должен быть добавлен автором установки пакета установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование функций установщика](using-installer-functions.md)
    -   [Инициализация приложения](initializing-an-application.md)
    -   [Диалоговое окно файла firstrun](firstrun-dialog.md)
    -   [Сведения о пользовательском интерфейсе](about-the-user-interface.md)

-   Создание приложений, использующих косвенную модель, для ссылки на компоненты с параллельными функциями. полные категории компонентов должны добавляться автором установки пакета установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Компоненты с квалификаторами](qualified-components.md)
    -   [Использование полных компонентов](using-qualified-components.md)

-   Используйте закрытые и параллельные сборки для изоляции приложений и уменьшения конфликтов DLL.

    Дополнительные сведения см. в следующих разделах:

    -   [Сборки](assemblies.md)
    -   [разделы реестра сборки, записанные установщик Windows](assembly-registry-keys-written-by-windows-installer-.md)
    -   [установка сборок Win32 для параллельного совместного использования в Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [установка сборок Win32 для частного использования приложения в Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [Таблица Мсиассембли](msiassembly-table.md)
    -   [Таблица Мсиассемблинаме](msiassemblyname-table.md)
    -   [**мсипровидеассембли**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**MsiWin32AssemblySupport, свойство**](msiwin32assemblysupport.md)
    -   [**Мсинетассемблисуппорт, свойство**](msinetassemblysupport.md)
    -   [**Изолированные компоненты**](isolated-components.md)

-   Подготовьте приложение для установки собственных основных обновлений.

    Дополнительные сведения см. в следующих разделах:

    -   [Установка исправлений и обновления](patching-and-upgrades.md)
    -   [Основные обновления](major-upgrades.md)
    -   [**UpgradeCode, свойство**](upgradecode.md)
    -   [**Использование UpgradeCode**](using-an-upgradecode.md)
    -   [Предотвращение установки старого пакета более новой версией](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Подготовьте приложение, чтобы установить собственные незначительные обновления, небольшие обновления или исправления.

    Дополнительные сведения см. в следующих разделах:

    -   [Установка исправлений и обновления](patching-and-upgrades.md)
    -   [Небольшие обновления](small-updates.md)
    -   [Незначительные обновления](minor-upgrades.md)

-   упорядочите ресурсы приложения в компоненты, которые могут работать с установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Windows Компоненты установщика](windows-installer-components.md)
    -   [Работа с функциями и компонентами](working-with-features-and-components.md)
    -   [Использование транзитивных компонентов](using-transitive-components.md)
    -   [Что произойдет, если правила компонентов будут разорваны?](what-happens-if-the-component-rules-are-broken.md)
    -   [Упорядочение приложений по компонентам](organizing-applications-into-components.md)
    -   [Изолированные компоненты](isolated-components.md)
    -   [Компоненты с квалификаторами](qualified-components.md)

## <a name="setup-authors"></a>Авторы программы установки

авторы программы установки создают установщик Windows пакеты (файлы .msi), которые содержат логику установки и сведения, необходимые для установки приложения. обычно они используют средства разработки, такие как [Orca.exe](orca-exe.md) для заполнения базы данных установщик Windows с помощью логики и информации программы установки. Как правило, авторы программы установки выполняют следующие действия:

-   определите функциональные возможности, доступные в разных версиях установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [определение версии установщик Windows](determining-the-windows-installer-version.md)
    -   [выпущенные версии установщик Windows](released-versions-of-windows-installer.md)
    -   [новые возможности установщик Windows](what-s-new-in-windows-installer.md)

-   упорядочивайте ресурсы приложений в установщик Windows компоненты.

    Дополнительные сведения см. в следующих разделах:

    -   [Windows Компоненты установщика](windows-installer-components.md)
    -   [Упорядочение приложений по компонентам](organizing-applications-into-components.md)
    -   [Изменение кода компонента](changing-the-component-code.md)
    -   [Что произойдет, если правила компонентов будут разорваны?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   используйте сторонние установщик Windows средства разработки пакетов или средства пакета SDK, такие как [Orca.exe](orca-exe.md) для заполнения базы данных установки и создания пакета установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Windows Средства разработки установщика](windows-installer-development-tools.md)
    -   [Пакет установки, сведения о базе данных установщика](installation-package.md)
    -   [Windows Расширения файлов установщика](windows-installer-file-extensions.md)
    -   [Таблицы базы данных](database-tables.md)
    -   [Коды пакетов](package-codes.md)
    -   [Создание большого пакета](authoring-a-large-package.md)
    -   [Windows Установщик на 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md)
    -   [Именование настраиваемых таблиц, свойств и действий](naming-custom-tables-properties-and-actions.md)
    -   [ограничения OLE на Потоки](ole-limitations-on-streams.md)
    -   [Формат определения столбца](column-definition-format.md)
    -   [Уменьшение размера файла .msi](reducing-the-size-of-an--msi-file.md)

-   создайте базу данных установщик Windows для установки файлов.

    Дополнительные сведения см. в следующих разделах:

    -   [Группа основных таблиц](core-tables-group.md)
    -   [Группа таблиц файлов](file-tables-group.md)
    -   [Таблица файлов](file-table.md)
    -   [Поиск файлов](file-searching.md)
    -   [Стоимость файлов](file-costing.md)
    -   [Установка файла](file-installation.md)
    -   [Сопутствующие файлы](companion-files.md)
    -   [Правила управления версиями файлов](file-versioning-rules.md)
    -   [Управление версиями файлов по умолчанию](default-file-versioning.md)
    -   [Замена существующих файлов](replacing-existing-files.md)
    -   [Использование ящиков и сжатых источников](using-cabinets-and-compressed-sources.md)
    -   [Удаление потерянных файлов](removing-stranded-files.md)
    -   [Установка постоянных компонентов, файлов, шрифтов, разделов реестра](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Таблица Филесфпкаталог](filesfpcatalog-table.md)
    -   [Поиск файла и создание свойства, содержащего путь к файлу](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Поиск каталога и файла в каталоге](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   создание установщик Windows базы данных, которая устанавливает структуру каталогов и папки.

    Дополнительные сведения см. в следующих разделах:

    -   [Группа основных таблиц](core-tables-group.md)
    -   [Группа таблиц файлов](file-tables-group.md)
    -   [Таблица компонентов](component-table.md)
    -   [Таблица каталога](directory-table.md)
    -   [Использование таблицы Directory](using-the-directory-table.md)
    -   [Использование свойства каталога в пути](using-a-directory-property-in-a-path.md)
    -   [Свойства системной папки](property-reference.md)
    -   [Таблица Креатефолдер](createfolder-table.md)
    -   [Таблица Локкпермиссионс](lockpermissions-table.md)
    -   [Таблица Мсилоккпермиссионсекс](msilockpermissionsex-table.md)
    -   [Изменение целевого расположения каталога](changing-the-target-location-for-a-directory.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   создайте базу данных установщик Windows, которая устанавливает разделы реестра.

    Дополнительные сведения см. в следующих разделах:

    -   [Группа основных таблиц](core-tables-group.md)
    -   [Группа таблиц реестра](registry-tables-group.md)
    -   [Таблица реестра](registry-table.md)
    -   [Изменение реестра](modifying-the-registry.md)
    -   [Добавление или удаление разделов реестра при установке или удалении компонентов](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Добавление и удаление приложения без трассировки в реестре](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Установка постоянных компонентов, файлов, шрифтов, разделов реестра](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Поиск существующих приложений, файлов, записей реестра или записей .ini файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Поиск записи реестра и создание свойства, содержащего значение реестра](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [разделы реестра сборки, записанные установщик Windows](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Удалить раздел реестра](uninstall-registry-key.md)
    -   [Таблица Селфрег](selfreg-table.md)
    -   [Указание порядка самостоятельной регистрации](specifying-the-order-of-self-registration.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   создание установщик Windows базы данных, которая устанавливает службы.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица Сервицеинсталл](serviceinstall-table.md)
    -   [Таблица ServiceControl](servicecontrol-table.md)
    -   [Таблица компонентов](component-table.md)

-   создайте базу данных установщик Windows, которая устанавливает изолированные компоненты или компоненты COM.

    Дополнительные сведения см. в следующих разделах:

    -   [Группа таблиц реестра](registry-tables-group.md)
    -   [Таблица классов](class-table.md)
    -   [Таблица ComPlus](complus-table.md)
    -   [Изолированные компоненты](isolated-components.md)
    -   [Использование изолированных компонентов](using-isolated-components.md)
    -   [Установка изолированных компонентов](installation-of-isolated-components.md)
    -   [Повторная установка изолированных компонентов](reinstallation-of-isolated-components.md)
    -   [Удаление изолированных компонентов](removal-of-isolated-components.md)
    -   [Установка COM-компонента в Закрытое расположение](installing-a-com-component-to-a-private-location.md)
    -   [Сделать компонент COM в существующем пакете частным](make-a-com-component-in-an-existing-package-private.md)
    -   [установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md)
    -   [Установка компонента, не являющегося компонентом COM, в Закрытое расположение](installing-a-non-com-component-to-a-private-location.md)
    -   [Создание частного компонента, не являющегося компонентом COM, в существующем пакете](make-a-non-com-component-in-an-existing-package-private.md)

-   создание установщик Windows базы данных, которая устанавливает сборки.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица Мсиассембли](msiassembly-table.md)
    -   [Таблица Мсиассемблинаме](msiassemblyname-table.md)
    -   [Сборки](assemblies.md)
    -   [разделы реестра сборки, записанные установщик Windows](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Установка сборок Win32](installation-of-win32-assemblies.md)

-   создайте базу данных установщик Windows, которая устанавливает драйверы и трансляторы ODBC.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица Одбкаттрибуте](odbcattribute-table.md)
    -   [Таблица Одбкдривер](odbcdriver-table.md)
    -   [Таблица Одбктранслатор](odbctranslator-table.md)
    -   [Таблица Одбкдатасаурце](odbcdatasource-table.md)
    -   [Таблица Одбксаурцеаттрибуте](odbcsourceattribute-table.md)

-   создание установщик Windows базы данных, которая устанавливает MIME.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица MIME](mime-table.md)
    -   [Таблица расширения](extension-table.md)
    -   [Изменение реестра](modifying-the-registry.md)

-   создайте базу данных установщик Windows, которая устанавливает переменные среды.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица среды](environment-table.md)

-   создание установщик Windows базы данных, которая устанавливает ярлыки.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица ярлыков](shortcut-table.md)
    -   [Таблица Мсишорткутпроперти](msishortcutproperty-table.md)
    -   [Изменение ярлыков установщика](editing-installer-shortcuts.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   создание установщик Windows базы данных, которая устанавливает несколько экземпляров приложений.

    Дополнительные сведения см. в следующих разделах:

    -   [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md)
    -   [Создание нескольких экземпляров с помощью преобразований экземпляров](authoring-multiple-instances-with-instance-transforms.md)
    -   [Установка нескольких экземпляров с преобразованиями экземпляров](installing-multiple-instances-with-instance-transforms.md)

-   Укажите состояния и параметры выбора компонентов по умолчанию.

    Дополнительные сведения см. в следующих разделах:

    -   [Группа основных таблиц](core-tables-group.md)
    -   [Таблица компонентов](component-table.md)
    -   [Таблица функций](feature-table.md)
    -   [Таблица Феатурекомпонентс](featurecomponents-table.md)
    -   [Управление состояниями выбора компонентов](controlling-feature-selection-states.md)
    -   [Свойства параметров установки компонентов](property-reference.md)

-   Укажите условия, которые должны быть удовлетворены для установки приложения или выбранных компонентов.

    Дополнительные сведения см. в следующих разделах:

    -   [Таблица условий](condition-table.md)
    -   [Таблица Лаунчкондитион](launchcondition-table.md)
    -   [Таблица компонентов](component-table.md)
    -   [Использование свойств в условных инструкциях](using-properties-in-conditional-statements.md)
    -   [Синтаксис условных операторов](conditional-statement-syntax.md)
    -   [Действия по обработке условий, выполняемые во время удаления](conditioning-actions-to-run-during-removal.md)
    -   [Примеры синтаксиса условных операторов](examples-of-conditional-statement-syntax.md)

-   Создайте последовательность действий, используемых для установки приложения.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование таблицы последовательностей](using-a-sequence-table.md)
    -   [Группа таблиц процедур установки](installation-procedure-tables-group.md)
    -   [Подробный пример таблицы последовательности](sequence-table-detailed-example.md)
    -   [Действия с ограничениями последовательности](actions-with-sequencing-restrictions.md)
    -   [Действия без ограничений на последовательность](actions-without-sequencing-restrictions.md)
    -   [Использование свойств в условных инструкциях](using-properties-in-conditional-statements.md)
    -   [Синтаксис условных операторов](conditional-statement-syntax.md)
    -   [Примеры синтаксиса условных операторов](examples-of-conditional-statement-syntax.md)
    -   [Действия по обработке условий, выполняемые во время удаления](conditioning-actions-to-run-during-removal.md)
    -   [Стандартные действия](standard-actions.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   подготовьте пакет установки приложения для будущих обновлений приложения с помощью службы установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Установка исправлений и обновления](patching-and-upgrades.md)
    -   [Подготовка приложения к будущим основным обновлениям](preparing-an-application-for-future-major-upgrades.md)
    -   [Использование UpgradeCode](using-an-upgradecode.md)
    -   [Обновление таблицы](upgrade-table.md)
    -   [**UpgradeCode, свойство**](upgradecode.md)
    -   [Предотвращение установки старого пакета более новой версией](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Изменение кода продукта](changing-the-product-code.md)
    -   [Обновление сборок](updating-assemblies.md)
    -   [Windows Примеры установщика](windows-installer-examples.md)

-   устранение неполадок установщик Windows пакетов в процессе разработки.

    Дополнительные сведения см. в следующих разделах:

    -   [Проверка пакета](package-validation.md)
    -   [Внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md)
    -   [Windows Ведение журнала установщика](windows-installer-logging.md)
    -   [Проверка установки компонентов, компонентов, файлов](checking-the-installation-of-features-components-files.md)
    -   [Создание большого пакета](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows Средства разработки установщика](windows-installer-development-tools.md)
    -   [Проверка модулей слияния](validating-merge-modules.md)
    -   [Проверка базы данных установки](validating-an-installation-database.md)
    -   [Проверка обновления установки](validating-an-installation-upgrade.md)
    -   [Поиск неработающей функции или компонента](searching-for-a-broken-feature-or-component.md)
    -   [Windows Сообщения об ошибках установщика](windows-installer-error-messages.md)
    -   [Ведение журнала запросов на перезагрузку](logging-of-reboot-requests.md)

-   Обеспечьте безопасную установку и установку приложения.

    Дополнительные сведения см. в следующих разделах:

    -   [Рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md)
    -   [Рекомендации по защите настраиваемых действий](guidelines-for-securing-custom-actions.md)
    -   [Безопасность настраиваемых действий](custom-action-security.md)
    -   [Рекомендации по защите пакетов на заблокированных компьютерах](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Создание полностью проверенной подписанной установки с помощью службы автоматизации](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Пример установки с применением установщика на базе URL](a-url-based-windows-installer-installation-example.md)
    -   [Создание пользовательского интерфейса для ввода пароля](authoring-the-user-interface-for-password-input.md)
    -   [цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md)
    -   [использование установщик Windows с UAC](using-windows-installer-with-uac.md)
    -   [Исправление контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**AdminUser, свойство**](adminuser.md)
    -   [**Привилегированное свойство**](privileged.md)
    -   [**Секурекустомпропертиес, свойство**](securecustomproperties.md)

-   Создайте пользовательский интерфейс для отображения параметров для настройки установки и получения сведений от пользователя о ожидающем процессе установки.

    Дополнительные сведения см. в следующих разделах:

    -   [Сведения о пользовательском интерфейсе](about-the-user-interface.md)
    -   [Добавление элементов управления и текста](adding-controls-and-text.md)
    -   [Создание элемента управления ProgressBar](authoring-a-progressbar-control.md)
    -   [Создание сообщений с приглашением на диск](authoring-disk-prompt-messages.md)
    -   [Создание условного выражения "Подождите..." Окно сообщения](authoring-a-conditional-please-wait-------message-box.md)
    -   [Предварительный просмотр пользовательского интерфейса](previewing-the-user-interface.md)
    -   [Добавление текста, хранящегося в свойстве](adding-text-stored-in-a-property.md)
    -   [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Создайте внешний пользовательский интерфейс, чтобы предоставить настраиваемый пользовательский интерфейс для настройки установки и получения от пользователя сведений о ожидающем процессе установки.

    Дополнительные сведения см. в следующих разделах:

    -   [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Мониторинг установки с помощью Мсисетекстерналуирекорд](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [синтаксический анализ сообщений установщик Windows](parsing-windows-installer-messages.md)
    -   [Возвращение значений из внешнего обработчика пользовательского интерфейса](returning-values-from-an-external-user-interface-handler.md)
    -   [\_обработчик инсталлуи](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Обработка сообщений о ходе выполнения с помощью Мсисетекстерналуи](handling-progress-messages-using-msisetexternalui.md)
    -   [Мониторинг установки с помощью Мсисетекстерналуи](monitoring-an-installation-using-msisetexternalui.md)

-   Задание сведений для приложения в окне " **Установка и удаление программ** " (ARP)

    Дополнительные сведения см. в следующих разделах:

    -   [настройка установки и удаления программ с помощью установщик Windows](configuring-add-remove-programs-with-windows-installer.md)
    -   [Добавление и удаление приложения без трассировки в реестре](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Удалить раздел реестра](uninstall-registry-key.md)

-   создание настраиваемых действий для обработки логики установки, которая изначально не поддерживается установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Настраиваемые действия](custom-actions.md)
    -   [Сводный список всех типов настраиваемых действий](summary-list-of-all-custom-action-types.md)
    -   [Рекомендации по защите настраиваемых действий](guidelines-for-securing-custom-actions.md)
    -   [Ссылка на настраиваемое действие](custom-action-reference.md)
    -   [Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Использование настраиваемого действия для запуска установленного файла в конце установки](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Доступ к базе данных или сеансу из настраиваемого действия](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Доступ к текущему сеансу установщика из пользовательского действия](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Изменение состояния системы с помощью настраиваемого действия](changing-the-system-state-using-a-custom-action.md)

-   начальная загрузка установщик Windows на компьютер пользователя.

    Дополнительные сведения см. в следующих разделах:

    -   [Начальная загрузка](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Начальная загрузка со скачиванием из Интернета](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Пример установки с применением установщика на базе URL](a-url-based-windows-installer-installation-example.md)
    -   [Настройка ресурсов Setup.exe](configuring-the-setup-exe-resources.md)
    -   [Загрузка установки из Интернета](downloading-an-installation-from-the-internet.md)

-   придерживайтесь Active Accessibility рекомендаций при написании пакетов установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Специальные возможности](accessibility.md)

-   Подготовьтесь к международной настройке приложения.

    Дополнительные сведения см. в следующих разделах:

    -   [подготовка пакета установщик Windows для локализации](preparing-a-windows-installer-package-for-localization.md),
    -   [локализация пакета установщик Windows](localizing-a-windows-installer-package.md)
    -   [обработка кодовой страницы (установщик Windows)](code-page-handling-windows-installer-.md)
    -   [Добавление локализованных ресурсов](adding-localized-resources.md)
    -   [Пример локализации](a-localization-example.md)
    -   [Локализация таблиц ошибок и Актионтекст](localizing-the-error-and-actiontext-tables.md)
    -   [Локализация столбцов базы данных](localizing-database-columns.md)
    -   [Создание базы данных со нейтральной кодовой страницей](creating-a-database-with-a-neutral-code-page.md)
    -   [Обработка кодовой страницы импортированных и экспортированных таблиц](code-page-handling-of-imported-and-exported-tables.md)
    -   [Локализация языка, отображаемого диалоговыми окнами](localizing-the-language-displayed-by-dialogs.md)
    -   [Импорт локализованных таблиц ошибок и Актионтекст](importing-localized-error-and-actiontext-tables.md)
    -   [Обновление свойств Продуктлангуаже и ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Обновление потока сводных данных](updating-a-summary-information-stream.md)
    -   [Компоненты с квалификаторами](qualified-components.md)
    -   [Таблица Уитекст](uitext-table.md)
    -   [Управление языком и кодовой страницей](manage-language-and-codepage.md)
    -   [Проверка кодовой страницы базы данных установки](checking-the-installation-database-code-page.md)

-   создание пакетов установщик Windows для 32-разрядных и 64-разрядных платформ.

    Дополнительные сведения см. в следующих разделах:

    -   [Windows Установщик на 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md)
    -   [64-разрядные пользовательские действия](64-bit-custom-actions.md)
    -   [Использование 64-разрядных настраиваемых действий](using-64-bit-custom-actions.md)
    -   [Использование 64-разрядных модулей слияния](using-64-bit-merge-modules.md)

-   распространение общих компонентов установщик Windows и логики установки в виде модулей слияния.

    Дополнительные сведения см. в следующих разделах:

    -   [Модули слияния](merge-modules.md)
    -   [Создание языкового преобразования для модуля многоязычного слияния](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Применение настраиваемого модуля слияния с настройками](applying-a-configurable-merge-module-with-customizations.md)

-   запланируйте или подавление перезагрузок во время установки установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Перезагрузка системы](system-reboots.md)
    -   [Ведение журнала запросов на перезагрузку](logging-of-reboot-requests.md)

-   Создание обновлений или исправлений для существующего приложения путем создания исправления.

    Дополнительные сведения см. в следующих разделах:

    -   [Создание небольшого исправления обновления](creating-a-small-update-patch.md)
    -   [Пример небольшого обновления исправлений](a-small-update-patching-example.md)

-   Создайте пакет с двойным набором, поддерживающий установку приложения либо только для текущего пользователя, либо для всех пользователей компьютера.

    Дополнительные сведения см. в следующих разделах:

    -   [Контекст установки](installation-context.md)
    -   [Создание отдельных пакетов](single-package-authoring.md)
    -   [Пример создания отдельного пакета](single-package-authoring-example.md)

-   настройка служб на компьютере с помощью установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование конфигурации служб](using-services-configuration.md)

-   защита ресурсов на компьютере с помощью установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md)
    -   [Защита ресурсов](securing-resources-.md)

-   Перечисление всех компонентов, установленных на компьютере, и получение пути к ключу для компонента.

    Дополнительные сведения см. в следующих разделах:

    -   [Перечисление компонентов](enumerating-components-.md)

-   Установка нескольких пакетов с помощью [*обработки транзакций*](t-gly.md).

    Дополнительные сведения см. в следующих разделах:

    -   [Установки с несколькими пакетами](multiple-package-installations.md)

-   внедрение настраиваемого пользовательского интерфейса в пакет установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование пользовательского интерфейса](using-the-user-interface.md)
    -   [Использование встроенного пользовательского интерфейса](using-an-embedded-ui.md)

## <a name="it-professionals"></a>ИТ-специалисты

ит-специалисты и администраторы настраивают и развертывают существующие пакеты установщик Windows. эти пользователи переупаковывают программы установки для существующих приложений в установщик Windows пакеты установки, а затем устанавливают и обслуживают административные образы установок установщик Windows в сетях.

-   настройка приложений и настроек с помощью создания и применения преобразований установщик Windows

    Дополнительные сведения см. в следующих разделах:

    -   [Настройка](customization.md)
    -   [Преобразования баз данных](database-transforms.md)
    -   [Пример преобразования настройки](a-customization-transform-example.md)
    -   [Слияния и преобразования](merges-and-transforms.md)
    -   [Использование преобразований для добавления ресурсов](using-transforms-to-add-resources.md)
    -   [Создание преобразования](generate-a-transform.md)
    -   [Параметры командной строки](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Применение преобразования](apply-a-transform.md)
    -   [Просмотр преобразования](view-a-transform.md)
    -   [Просмотр различий между двумя базами данных](view-differences-between-two-databases.md)
    -   [Исправление настроенных приложений](patching-customized-applications.md)

-   развертывание пакета установки установщик Windows, обновления или исправления.

    Дополнительные сведения см. в следующих разделах:

    -   [Установка приложения](installing-an-application.md)
    -   [Установка исправлений и обновления](patching-and-upgrades.md)
    -   [Преобразования](transforms.md)
    -   [Установка пакета с повышенными привилегиями для без прав администратора](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Применение основных обновлений путем исправления локальной установки продукта](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Применение основных обновлений путем установки продукта](applying-major-upgrades-by-installing-the-product.md)
    -   [Применение небольших обновлений путем исправления локальной установки продукта](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Применение небольших обновлений путем переустановки продукта](applying-small-updates-by-reinstalling-the-product.md)
    -   [Применение небольших обновлений путем исправления административного образа](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Установка исправлений первоначальных установок](patching-initial-installations.md)
    -   [Параметры командной строки](command-line-options.md)

-   устранение неполадок установщик Windows пакетов.

    Дополнительные сведения см. в следующих разделах:

    -   [Windows Ведение журнала установщика](windows-installer-logging.md)
    -   [Проверка установки компонентов, компонентов, файлов](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Поиск неработающей функции или компонента](searching-for-a-broken-feature-or-component.md)
    -   [Windows Сообщения об ошибках установщика](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   используйте скрипты для запроса пакетов установщик Windows для получения сведений о продукте и изменения установки.

    Дополнительные сведения см. в следующих разделах:

    -   [Интерфейс автоматизации](automation-interface.md)
    -   [Windows Примеры сценариев для установщика](windows-installer-scripting-examples.md)
    -   [использование установщик Windows с WMI](using-windows-installer-with-wmi.md)

-   Создание и обслуживание административных установок.

    Дополнительные сведения см. в следующих разделах:

    -   [Административная установка](administrative-installation.md)
    -   [Параметры командной строки](command-line-options.md)
    -   [**Админпропертиес, свойство**](adminproperties.md)
    -   [Применение небольших обновлений путем исправления административного образа](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Применение пакета исправлений к административной установке](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Порядок выполнения действия](action-execution-order.md)
    -   [**Исадминпаккаже, свойство**](isadminpackage.md)
    -   [Порядок приоритета свойств](order-of-property-precedence.md)
    -   [**Админпропертиес, свойство**](adminproperties.md)

-   Сделать приложение доступным только для всех пользователей компьютера или только для указанного пользователя.

    Дополнительные сведения см. в следующих разделах:

    -   [Контекст установки](installation-context.md)
    -   [**Свойство ALLUSERS**](allusers.md)

-   Анализ пакетов, установка продуктов и Настройка параметров функций с помощью командной строки.

    Дополнительные сведения см. в следующих разделах:

    -   [Параметры командной строки](command-line-options.md)
    -   [Установка значений открытых свойств в командной строке](setting-public-property-values-on-the-command-line.md)
    -   [Получение и задание свойств](getting-and-setting-properties.md)
    -   [Переустановка компонента или приложения](reinstalling-a-feature-or-application.md)
    -   [Применение небольших обновлений путем исправления локальной установки продукта](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Применение небольших обновлений путем переустановки продукта](applying-small-updates-by-reinstalling-the-product.md)
    -   [Изменение целевого расположения каталога](changing-the-target-location-for-a-directory.md)
    -   [Применение небольших обновлений путем исправления административного образа](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Применение основных обновлений путем установки продукта](applying-major-upgrades-by-installing-the-product.md)
    -   [Свойства конфигурации](property-reference.md)
    -   [Свойства параметров установки компонентов](property-reference.md)

-   Работа с политикой для управления правами доступа и разрешениями.

    Дополнительные сведения см. в следующих разделах:

    -   [Политики компьютера](machine-policies.md),
    -   [Политики пользователя](user-policies.md),
    -   [Установка пакета с повышенными привилегиями для без прав администратора](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Объявление приложения Per-User для установки с повышенными привилегиями](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser, свойство**](adminuser.md)
    -   [**Привилегированное свойство**](privileged.md)
    -   [**Енаблеусерконтрол, свойство**](enableusercontrol.md)
    -   [**Свойство "значение"**](usersid.md)
    -   [**Секурекустомпропертиес, свойство**](securecustomproperties.md)

-   Установка нескольких пакетов с помощью [*обработки транзакций*](t-gly.md).

    Дополнительные сведения см. в следующих разделах:

    -   [Установки с несколькими пакетами](multiple-package-installations.md)

-   внедрение настраиваемого пользовательского интерфейса в пакет установщик Windows.

    Дополнительные сведения см. в следующих разделах:

    -   [Использование пользовательского интерфейса](using-the-user-interface.md)
    -   [Использование встроенного пользовательского интерфейса](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Разработчики инфраструктуры

разработчики инфраструктуры могут создавать унифицированные платформы для развертывания программного обеспечения, использующего службу установщик Windows, и управления им. они могут использовать программный интерфейс установщик Windows для запроса, управления и распространения приложений, исправлений и источников в системе.

-   Поиск, Инвентаризация и запрос сведений о состоянии, информации и клиентах компонентов.

    Дополнительные сведения см. в следующих разделах:

    -   [Функции для конкретных компонентов](installer-function-reference.md)
    -   [Функции состояния системы](installer-function-reference.md)
    -   [Объект установщика](installer-object.md)
    -   [Объект Product](product-object.md)
    -   [Объект Patch](patch-object.md)

-   Инвентаризация и запрос информации и состояния продуктов и функций.

    Дополнительные сведения см. в следующих разделах:

    -   [Инвентаризация продуктов и исправлений](inventory-products-and-patches-.md)
    -   [Функции состояния системы](installer-function-reference.md)
    -   [Функции запроса продукта](installer-function-reference.md)
    -   [Объект установщика](installer-object.md)
    -   [Объект Product](product-object.md)
    -   [Объект Patch](patch-object.md)

-   повышение устойчивости источника с помощью установщик Windows для инвентаризации, запроса и изменения исходного списка приложений, обновлений и исправлений.

    Дополнительные сведения см. в следующих разделах:

    -   [**Свойство SOURCELIST**](sourcelist.md)
    -   [**Отказоустойчивость источника**](source-resiliency.md)
    -   [Функции установки и настройки](installer-function-reference.md)
    -   [Объект установщика](installer-object.md)
    -   [Объект Product](product-object.md)
    -   [Объект Patch](patch-object.md)

-   повышение отказоустойчивости источника с помощью установщик Windows для инвентаризации, запроса и изменения источников мультимедиа.

    Дополнительные сведения см. в следующих разделах:

    -   [**Свойство SOURCELIST**](sourcelist.md)
    -   [Отказоустойчивость источника](source-resiliency.md)
    -   [Функции установки и настройки](installer-function-reference.md)
    -   [Объект Product](product-object.md)
    -   [Объект Patch](patch-object.md)

-   Инвентаризация и запрос информации и состояния исправлений.

    Дополнительные сведения см. в следующих разделах:

    -   [Инвентаризация продуктов и исправлений](inventory-products-and-patches-.md)
    -   [Справочник по функциям установщика](installer-function-reference.md)
    -   [Объект Patch](patch-object.md)

-   Работа с политикой для управления правами доступа и разрешениями.

    Дополнительные сведения см. в следующих разделах:

    -   [Политики компьютера](machine-policies.md)
    -   [Политики пользователя](user-policies.md)
    -   [Установка пакета с повышенными привилегиями для без прав администратора](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Объявление приложения Per-User для установки с повышенными привилегиями](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser, свойство**](adminuser.md)
    -   [**Привилегированное свойство**](privileged.md)
    -   [**Енаблеусерконтрол, свойство**](enableusercontrol.md)
    -   [**Свойство "значение"**](usersid.md)
    -   [**Секурекустомпропертиес, свойство**](securecustomproperties.md)

 

 



