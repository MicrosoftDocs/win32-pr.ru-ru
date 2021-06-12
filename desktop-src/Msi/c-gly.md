---
description: Сведения о установщик Windows концепциях, начинающихся с буквы C, например CAB-файл и контрольная сумма.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010927"
---
# <a name="c-windows-installer"></a><span data-ttu-id="69abe-103">C (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="69abe-103">C (Windows Installer)</span></span>

<span data-ttu-id="69abe-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="69abe-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="69abe-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**CAB-файл**</span><span class="sxs-lookup"><span data-stu-id="69abe-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-106">Один файл, обычно с расширением .cab, в котором хранятся сжатые файлы в библиотеке файлов.</span><span class="sxs-lookup"><span data-stu-id="69abe-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="69abe-107">Формат CAB является эффективным способом упаковки нескольких файлов, поскольку сжатие выполняется по границам файлов, значительно повышая степень сжатия.</span><span class="sxs-lookup"><span data-stu-id="69abe-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="69abe-108">Сведения о создании ящиков см. в разделе [CAB-файлы](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="69abe-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**вычислен**</span><span class="sxs-lookup"><span data-stu-id="69abe-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-110">Вычисленное значение, которое зависит от содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="69abe-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="69abe-111">Он хранится с данными для обнаружения повреждения файла.</span><span class="sxs-lookup"><span data-stu-id="69abe-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="69abe-112">Система проверяет это значение, чтобы убедиться, что данные не повреждены.</span><span class="sxs-lookup"><span data-stu-id="69abe-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="69abe-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**см**</span><span class="sxs-lookup"><span data-stu-id="69abe-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-114">Наименьшая часть установки, обрабатываемая установщиком, а также компоновочный блок приложения или функции с точки зрения программиста.</span><span class="sxs-lookup"><span data-stu-id="69abe-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="69abe-115">Примерами компонентов являются группы связанных файлов, COM-объект или библиотека.</span><span class="sxs-lookup"><span data-stu-id="69abe-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="69abe-116">Дополнительные сведения см. в разделе [компоненты и компоненты](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="69abe-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**Фиксация баз данных**</span><span class="sxs-lookup"><span data-stu-id="69abe-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-118">Накопленные изменения, внесенные в базу данных.</span><span class="sxs-lookup"><span data-stu-id="69abe-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="69abe-119">Изменения не отражаются в реальной базе данных до тех пор, пока база данных не будет зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="69abe-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="69abe-120">Дополнительные сведения см. в разделе [фиксация баз данных](committing-databases.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="69abe-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**Таблице ControlEvent событие**</span><span class="sxs-lookup"><span data-stu-id="69abe-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-122">Аспект функциональных возможностей пользовательского интерфейса установщика.</span><span class="sxs-lookup"><span data-stu-id="69abe-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="69abe-123">Типичная таблице ControlEvent событие запускает некоторое действие установщиком при активации элемента управления диалогового окна или другого события.</span><span class="sxs-lookup"><span data-stu-id="69abe-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="69abe-124">Дополнительные сведения см. в разделе [таблице ControlEvent событие Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="69abe-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**затрат**</span><span class="sxs-lookup"><span data-stu-id="69abe-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-126">Метод, используемый установщиком для определения требований к месту на диске для установки.</span><span class="sxs-lookup"><span data-stu-id="69abe-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="69abe-127">Стоимость учитывает такие факторы, как необходимость перезаписи существующих файлов.</span><span class="sxs-lookup"><span data-stu-id="69abe-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="69abe-128">Дополнительные сведения см. в разделе [стоимость файлов](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="69abe-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**файл. cub**</span><span class="sxs-lookup"><span data-stu-id="69abe-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-130">Модуль проверки, который хранит и предоставляет доступ к настраиваемым действиям ICE.</span><span class="sxs-lookup"><span data-stu-id="69abe-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="69abe-131">Дополнительные сведения см. в разделе [Sample. cub File](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="69abe-132">Дополнительные сведения см. в разделе также [установщик Windows расширения файлов](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="69abe-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**настраиваемое действие**</span><span class="sxs-lookup"><span data-stu-id="69abe-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="69abe-134">Написано автором [*пакета*](p-gly.md) , но не встроенным в установщик как стандартное действие.</span><span class="sxs-lookup"><span data-stu-id="69abe-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="69abe-135">Дополнительные сведения см. в разделе [Custom Actions](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="69abe-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



