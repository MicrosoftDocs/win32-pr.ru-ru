---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156322"
---
# <a name="p-windows-installer"></a><span data-ttu-id="62190-103">P (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="62190-103">P (Windows Installer)</span></span>

<span data-ttu-id="62190-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="62190-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="62190-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**пакеты**</span><span class="sxs-lookup"><span data-stu-id="62190-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="62190-106">[*файл MSI*](m-gly.md) и все [*Внешние исходные файлы*](e-gly.md) , на которые может указывать этот файл.</span><span class="sxs-lookup"><span data-stu-id="62190-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="62190-107">Таким образом, пакет содержит все сведения, необходимые установщик Windows для запуска пользовательского интерфейса и установки или удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="62190-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="62190-108">Дополнительные сведения см. в разделе также [*база данных установщика*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="62190-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="62190-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**код пакета**</span><span class="sxs-lookup"><span data-stu-id="62190-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="62190-110">Идентификатор GUID, определяющий конкретный пакет.</span><span class="sxs-lookup"><span data-stu-id="62190-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="62190-111">Уникальный код пакета является обязательным, так как некоторые преобразования или пакеты исправлений могут применяться к нескольким приложениям или могут обновить приложение в другом приложении или версии.</span><span class="sxs-lookup"><span data-stu-id="62190-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="62190-112">Дополнительные сведения см. в разделе [коды пакетов](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="62190-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="62190-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**исправления**</span><span class="sxs-lookup"><span data-stu-id="62190-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="62190-114">Метод обновления файла, который заменяет только изменяемые биты, а не весь файл.</span><span class="sxs-lookup"><span data-stu-id="62190-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="62190-115">Это означает, что пользователи могут загрузить обновление для продукта, который намного меньше, чем весь продукт.</span><span class="sxs-lookup"><span data-stu-id="62190-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="62190-116">Дополнительные сведения см. в разделе [пакеты исправлений](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="62190-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="62190-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**файл исправления**</span><span class="sxs-lookup"><span data-stu-id="62190-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="62190-118">[Пакет P атч](patch-packages.md) , используемый для установки исправлений.</span><span class="sxs-lookup"><span data-stu-id="62190-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="62190-119">Дополнительные сведения см. в разделе [Установка исправлений и обновления](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="62190-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="62190-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**режим предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="62190-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="62190-121">Режим для просмотра макета пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62190-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="62190-122">Дополнительные сведения см. [в разделе Предварительный просмотр пользовательского интерфейса](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="62190-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="62190-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**индикатор выполнения**</span><span class="sxs-lookup"><span data-stu-id="62190-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="62190-124">Управление, которое может отображаться установщиком во время выполнения сценария, представляющее ход установки.</span><span class="sxs-lookup"><span data-stu-id="62190-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="62190-125">Дополнительные сведения см. [в разделе Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="62190-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="62190-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**свойства**</span><span class="sxs-lookup"><span data-stu-id="62190-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="62190-127">Глобальные переменные, используемые во время установки.</span><span class="sxs-lookup"><span data-stu-id="62190-127">Global variables used during an installation.</span></span> <span data-ttu-id="62190-128">(См. раздел [о свойствах](about-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="62190-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="62190-129">Термин "свойство" также ссылается на атрибут объекта автоматизации.</span><span class="sxs-lookup"><span data-stu-id="62190-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="62190-130">(См. раздел [интерфейс автоматизации](automation-interface.md).)</span><span class="sxs-lookup"><span data-stu-id="62190-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="62190-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Publish**</span><span class="sxs-lookup"><span data-stu-id="62190-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="62190-132">Метод [*объявления*](a-gly.md) функции или приложения.</span><span class="sxs-lookup"><span data-stu-id="62190-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="62190-133">Публикация не заполняет пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="62190-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="62190-134">Однако, если другое приложение пытается открыть опубликованное приложение, установщику будет назначено достаточно информации для назначения опубликованного приложения.</span><span class="sxs-lookup"><span data-stu-id="62190-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="62190-135">Дополнительные сведения см. в разделе [*назначение*](a-gly.md) и [компоненты](components-and-features.md)и компоненты.</span><span class="sxs-lookup"><span data-stu-id="62190-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



