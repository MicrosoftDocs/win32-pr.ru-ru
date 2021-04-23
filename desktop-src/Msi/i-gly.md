---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910924"
---
# <a name="i-windows-installer"></a><span data-ttu-id="25f76-103">I (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="25f76-103">I (Windows Installer)</span></span>

<span data-ttu-id="25f76-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р. J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="25f76-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="25f76-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**файл IDT**</span><span class="sxs-lookup"><span data-stu-id="25f76-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-106">Таблица базы данных установщика экспортирована.</span><span class="sxs-lookup"><span data-stu-id="25f76-106">Exported installer database table.</span></span> <span data-ttu-id="25f76-107">Дополнительные сведения см. в разделе [Импорт и экспорт](importing-and-exporting.md) и [установщик Windows расширений файлов](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Импорт таблицы адресов (IAT)**</span><span class="sxs-lookup"><span data-stu-id="25f76-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-109">Где сохраненный виртуальный адрес сохраняется из каждой функции, импортированной из всех библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="25f76-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="25f76-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**внутренний пользовательский интерфейс**</span><span class="sxs-lookup"><span data-stu-id="25f76-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-111">Встроенные возможности установщика, которые можно использовать для создания графического пользовательского интерфейса для установки.</span><span class="sxs-lookup"><span data-stu-id="25f76-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="25f76-112">Автор может выбрать [*внешний пользовательский интерфейс*](e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="25f76-113">Дополнительные сведения см. [в разделе о пользовательском интерфейсе](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**уровень установки**</span><span class="sxs-lookup"><span data-stu-id="25f76-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-115">Указанное значение установки.</span><span class="sxs-lookup"><span data-stu-id="25f76-115">Specified installation value.</span></span> <span data-ttu-id="25f76-116">Приложение устанавливается, только если его собственный уровень меньше или равен уровню установки.</span><span class="sxs-lookup"><span data-stu-id="25f76-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="25f76-117">Поэтому набор приложений, выбранных для установки, можно изменить, изменив уровень установки.</span><span class="sxs-lookup"><span data-stu-id="25f76-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="25f76-118">Дополнительные сведения см. в разделе [Таблица функций](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**Установка по запросу**</span><span class="sxs-lookup"><span data-stu-id="25f76-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-120">Служба, устанавливающая приложения или компоненты по запросу пользователя или другого приложения.</span><span class="sxs-lookup"><span data-stu-id="25f76-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="25f76-121">[*Реклама*](a-gly.md) делает функцию или приложение доступной для установки по требованию.</span><span class="sxs-lookup"><span data-stu-id="25f76-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="25f76-122">Дополнительные сведения см. в статье [Установка по запросу](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**контекст установки**</span><span class="sxs-lookup"><span data-stu-id="25f76-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-124">Сочетание прав установки и типов установки создает три разных контекста установки: управление без управления, управление на уровне пользователя и управляемый компьютером.</span><span class="sxs-lookup"><span data-stu-id="25f76-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="25f76-125">Нет таких целей, как управление компьютерами без управления.</span><span class="sxs-lookup"><span data-stu-id="25f76-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="25f76-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**необходимость**</span><span class="sxs-lookup"><span data-stu-id="25f76-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-127">[*Установщик Windows*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**база данных установщика**</span><span class="sxs-lookup"><span data-stu-id="25f76-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-129">Реляционная база данных, содержащая инструкции по настройке для установки.</span><span class="sxs-lookup"><span data-stu-id="25f76-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="25f76-130">База данных установщика хранится в MSI- [*файле*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="25f76-131">Дополнительные сведения см. в разделе [база данных установщика](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**Функция установщика**</span><span class="sxs-lookup"><span data-stu-id="25f76-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-133">Вызывается пользователем или приложением для получения служб и функций установщика.</span><span class="sxs-lookup"><span data-stu-id="25f76-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="25f76-134">Это прикладной программный интерфейс установщика.</span><span class="sxs-lookup"><span data-stu-id="25f76-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="25f76-135">Дополнительные сведения см. в разделе [Справочник по функциям установщика](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="25f76-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**средство разработки пакета установщика**</span><span class="sxs-lookup"><span data-stu-id="25f76-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-137">Программное обеспечение, позволяющее разработчику создавать и изменять [*MSI-файл*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="25f76-138">Вместе с любыми [*внешними исходными файлами*](e-gly.md) состоит [*пакет*](p-gly.md) , содержащий все сведения, необходимые для установки.</span><span class="sxs-lookup"><span data-stu-id="25f76-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="25f76-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**внутренние исходные файлы**</span><span class="sxs-lookup"><span data-stu-id="25f76-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="25f76-140">Хранится в [*файле MSI*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="25f76-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="25f76-141">Несколько внутренних исходных файлов можно сжать и хранить вместе в CAB- [*файле*](c-gly.md) , который хранится в MSI-файле.</span><span class="sxs-lookup"><span data-stu-id="25f76-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



