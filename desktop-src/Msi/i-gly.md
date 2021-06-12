---
description: Сведения о установщик Windows основных понятиях, начинающихся с буквы I, например таблицы импорта адресов и уровня установки.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010657"
---
# <a name="i-windows-installer"></a>I (установщик Windows)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р. J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**файл IDT**
</dt> <dd>

Таблица базы данных установщика экспортирована. Дополнительные сведения см. в разделе [Импорт и экспорт](importing-and-exporting.md) и [установщик Windows расширений файлов](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Импорт таблицы адресов (IAT)**
</dt> <dd>

Где сохраненный виртуальный адрес сохраняется из каждой функции, импортированной из всех библиотек DLL.

</dd> <dt>

<span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**внутренний пользовательский интерфейс**
</dt> <dd>

Встроенные возможности установщика, которые можно использовать для создания графического пользовательского интерфейса для установки. Автор может выбрать [*внешний пользовательский интерфейс*](e-gly.md). Дополнительные сведения см. [в разделе о пользовательском интерфейсе](about-the-user-interface.md).

</dd> <dt>

<span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**уровень установки**
</dt> <dd>

Указанное значение установки. Приложение устанавливается, только если его собственный уровень меньше или равен уровню установки. Поэтому набор приложений, выбранных для установки, можно изменить, изменив уровень установки. Дополнительные сведения см. в разделе [Таблица функций](feature-table.md).

</dd> <dt>

<span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**Установка по запросу**
</dt> <dd>

Служба, устанавливающая приложения или компоненты по запросу пользователя или другого приложения. [*Реклама*](a-gly.md) делает функцию или приложение доступной для установки по требованию. Дополнительные сведения см. в статье [Установка по запросу](installation-on-demand.md).

</dd> <dt>

<span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**контекст установки**
</dt> <dd>

Сочетание прав установки и типов установки создает три разных контекста установки: управление без управления, управление на уровне пользователя и управляемый компьютером. Нет таких целей, как управление компьютерами без управления.

</dd> <dt>

<span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**необходимость**
</dt> <dd>

[*Установщик Windows*](m-gly.md).

</dd> <dt>

<span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**база данных установщика**
</dt> <dd>

Реляционная база данных, содержащая инструкции по настройке для установки. База данных установщика хранится в [*файле.msi*](m-gly.md). Дополнительные сведения см. в разделе [база данных установщика](installer-database.md).

</dd> <dt>

<span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**Функция установщика**
</dt> <dd>

Вызывается пользователем или приложением для получения служб и функций установщика. Это прикладной программный интерфейс установщика. Дополнительные сведения см. в разделе [Справочник по функциям установщика](installer-function-reference.md).

</dd> <dt>

<span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**средство разработки пакета установщика**
</dt> <dd>

Программное обеспечение, позволяющее разработчику создавать и изменять [*файл.msi*](m-gly.md). Вместе с любыми [*внешними исходными файлами*](e-gly.md) состоит [*пакет*](p-gly.md) , содержащий все сведения, необходимые для установки.

</dd> <dt>

<span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**внутренние исходные файлы**
</dt> <dd>

Хранится в [*файле.msi*](m-gly.md). Несколько внутренних исходных файлов можно сжать и хранить вместе в CAB- [*файле*](c-gly.md) , который хранится в файле .msi.

</dd> </dl>

 

 



