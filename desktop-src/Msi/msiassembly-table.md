---
description: В таблице Мсиассембли указаны параметры установщик Windows для сборок платформы Microsoft .NET и сборок Win32. Дополнительные сведения см. в разделе Установка сборок в глобальный кэш сборок и установка сборок Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Таблица Мсиассембли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999595"
---
# <a name="msiassembly-table"></a><span data-ttu-id="e91fc-104">Таблица Мсиассембли</span><span class="sxs-lookup"><span data-stu-id="e91fc-104">MsiAssembly Table</span></span>

<span data-ttu-id="e91fc-105">В таблице Мсиассембли указаны параметры установщик Windows для сборок платформы Microsoft .NET и сборок Win32.</span><span class="sxs-lookup"><span data-stu-id="e91fc-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="e91fc-106">Дополнительные сведения см. [в разделе Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="e91fc-107">В Windows XP установщик Windows может устанавливать сборки Win32 как [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="e91fc-108">Дополнительные сведения см. в разделе [параллельная сборка API](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="e91fc-109">**Windows 2000:** Эта функция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e91fc-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="e91fc-110">Таблица Мсиассембли содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e91fc-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="e91fc-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="e91fc-111">Column</span></span>            | <span data-ttu-id="e91fc-112">Type</span><span class="sxs-lookup"><span data-stu-id="e91fc-112">Type</span></span>                         | <span data-ttu-id="e91fc-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="e91fc-113">Key</span></span> | <span data-ttu-id="e91fc-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="e91fc-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="e91fc-115">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="e91fc-115">Component\_</span></span>       | [<span data-ttu-id="e91fc-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e91fc-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="e91fc-117">Да</span><span class="sxs-lookup"><span data-stu-id="e91fc-117">Y</span></span>   | <span data-ttu-id="e91fc-118">Нет</span><span class="sxs-lookup"><span data-stu-id="e91fc-118">N</span></span>        |
| <span data-ttu-id="e91fc-119">Функция\_</span><span class="sxs-lookup"><span data-stu-id="e91fc-119">Feature\_</span></span>         | [<span data-ttu-id="e91fc-120">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e91fc-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="e91fc-121">Нет</span><span class="sxs-lookup"><span data-stu-id="e91fc-121">N</span></span>   | <span data-ttu-id="e91fc-122">Нет</span><span class="sxs-lookup"><span data-stu-id="e91fc-122">N</span></span>        |
| <span data-ttu-id="e91fc-123">\_Манифест файла</span><span class="sxs-lookup"><span data-stu-id="e91fc-123">File\_Manifest</span></span>    | [<span data-ttu-id="e91fc-124">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e91fc-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="e91fc-125">Нет</span><span class="sxs-lookup"><span data-stu-id="e91fc-125">N</span></span>   | <span data-ttu-id="e91fc-126">Да</span><span class="sxs-lookup"><span data-stu-id="e91fc-126">Y</span></span>        |
| <span data-ttu-id="e91fc-127">\_Приложение файла</span><span class="sxs-lookup"><span data-stu-id="e91fc-127">File\_Application</span></span> | [<span data-ttu-id="e91fc-128">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e91fc-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="e91fc-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e91fc-129">N</span></span>   | <span data-ttu-id="e91fc-130">Да</span><span class="sxs-lookup"><span data-stu-id="e91fc-130">Y</span></span>        |
| <span data-ttu-id="e91fc-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e91fc-131">Attributes</span></span>        | [<span data-ttu-id="e91fc-132">Integer</span><span class="sxs-lookup"><span data-stu-id="e91fc-132">Integer</span></span>](integer.md)       | <span data-ttu-id="e91fc-133">Нет</span><span class="sxs-lookup"><span data-stu-id="e91fc-133">N</span></span>   | <span data-ttu-id="e91fc-134">Да</span><span class="sxs-lookup"><span data-stu-id="e91fc-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e91fc-135">Столбцы</span><span class="sxs-lookup"><span data-stu-id="e91fc-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e91fc-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="e91fc-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e91fc-137">Ключ в [таблице Component](component-table.md) , указывающий компонент установщик Windows, который содержит эту сборку.</span><span class="sxs-lookup"><span data-stu-id="e91fc-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="e91fc-138">Значение в этом поле не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="e91fc-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="e91fc-139">Поле ключевого пути компонента в [таблице Component](component-table.md) не должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e91fc-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="e91fc-140">Для сборок Win32 ключевой путь к компоненту не может быть файлом манифеста, указанным в файле \_ manifest.</span><span class="sxs-lookup"><span data-stu-id="e91fc-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="e91fc-141">Манифест может быть ключевой страницей для платформа .NET Framework или сборки политики.</span><span class="sxs-lookup"><span data-stu-id="e91fc-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="e91fc-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="e91fc-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="e91fc-143">Ключ в [таблицу функций](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="e91fc-144">Если сборка должна быть установлена при установке компонента, установщик Windows устанавливает компонент, указанный в этом поле.</span><span class="sxs-lookup"><span data-stu-id="e91fc-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="e91fc-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>\_Манифест файла</span><span class="sxs-lookup"><span data-stu-id="e91fc-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="e91fc-146">Внешний ключ в [таблице File](file-table.md) , указывающий файл, содержащий манифест сборки платформа .NET Framework или сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="e91fc-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="e91fc-147">Для сборки Win32 не указывайте этот файл в качестве файла пути к ключу компонента в поле ключевой путь [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91fc-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>\_Приложение файла</span><span class="sxs-lookup"><span data-stu-id="e91fc-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="e91fc-149">Чтобы установить сборку в частном расположении, введите в этом поле файл пути к ключу для компонента сборки.</span><span class="sxs-lookup"><span data-stu-id="e91fc-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="e91fc-150">Это значение, которое отображается в поле ключевого пути [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="e91fc-151">Установщик может установить сборку в структуру каталогов компонента, указанного в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="e91fc-152">Если сборка должна быть установлена в глобальный кэш сборок, это поле должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e91fc-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="e91fc-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибута</span><span class="sxs-lookup"><span data-stu-id="e91fc-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e91fc-154">Введите значение 1 (одно) для сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="e91fc-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="e91fc-155">Введите значение 0 (ноль) для платформа .NET Framework сборки.</span><span class="sxs-lookup"><span data-stu-id="e91fc-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="e91fc-156">Если столбец Attributes имеет значение NULL, установщик рассматривает сборку как сборку платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e91fc-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e91fc-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e91fc-157">Remarks</span></span>

<span data-ttu-id="e91fc-158">Если в таблице Мсиассембли есть хотя бы одна запись, [Таблица инсталлексекутесекуенце](installexecutesequence-table.md) должна содержать [действие Мсипублишассемблиес](msipublishassemblies-action.md)и [мсиунпублишассемблиес действие](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="e91fc-159">Поскольку откат сборок после их фиксации невозможен, установщик Windows использует двухэтапный процесс установки.</span><span class="sxs-lookup"><span data-stu-id="e91fc-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="e91fc-160">Интерфейсы для сборок создаются во время операций установки, создаваемых [действием мсипублишассемблиес](msipublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="e91fc-161">Сборки не фиксируются до успешного выполнения [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="e91fc-162">Это означает, что при создании настраиваемого действия или ресурса, основанного на сборке, она должна быть упорядочена после [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="e91fc-163">Например, если необходимо запустить службу, которая зависит от сборки в глобальном кэше сборок (GAC), необходимо запланировать запуск этой службы после выполнения [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e91fc-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="e91fc-164">Это означает, что нельзя использовать [таблицу ServiceControl](servicecontrol-table.md) для запуска службы, вместо этого необходимо использовать настраиваемое действие, виртуализированное после функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="e91fc-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="e91fc-165">Проверка</span><span class="sxs-lookup"><span data-stu-id="e91fc-165">Validation</span></span>

<dl>

[<span data-ttu-id="e91fc-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="e91fc-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e91fc-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="e91fc-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e91fc-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="e91fc-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e91fc-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="e91fc-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="e91fc-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="e91fc-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="e91fc-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="e91fc-171">ICE94</span></span>](ice94.md)  
</dl>

 

 
