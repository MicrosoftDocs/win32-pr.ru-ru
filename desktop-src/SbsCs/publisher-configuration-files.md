---
description: Файл конфигурации издателя — это XML-файл, который глобально перенаправляет приложения и сборки от использования одной версии параллельной сборки к другой версии той же сборки.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Файлы конфигурации издателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912507"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="eb3a0-103">Файлы конфигурации издателя</span><span class="sxs-lookup"><span data-stu-id="eb3a0-103">Publisher Configuration Files</span></span>

<span data-ttu-id="eb3a0-104">Файл конфигурации издателя — это XML-файл, который глобально перенаправляет приложения и сборки от использования одной версии параллельной сборки к другой версии той же сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="eb3a0-105">Как правило, издатель сборки создает совместимое обновление или исправление безопасности для каждой сборки, выдавая файл конфигурации издателя вместе с обновлением пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="eb3a0-106">Это называется [конфигурацией издателя](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="eb3a0-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="eb3a0-107">Дополнительные сведения об этом типе [конфигурации](configuration.md) см. в разделе Конфигурация издателя.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="eb3a0-108">Файлы конфигурации издателя имеют следующие элементы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="eb3a0-109">Полный список схем XML см. в разделе [Схема файла конфигурации издателя](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="eb3a0-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="eb3a0-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb3a0-110">Element</span></span>               | <span data-ttu-id="eb3a0-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="eb3a0-111">Attributes</span></span>                | <span data-ttu-id="eb3a0-112">Обязательно</span><span class="sxs-lookup"><span data-stu-id="eb3a0-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="eb3a0-113">**сборок**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-113">**assembly**</span></span>          |                           | <span data-ttu-id="eb3a0-114">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-114">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-115">**манифестверсион**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-115">**manifestVersion**</span></span>       | <span data-ttu-id="eb3a0-116">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-116">Yes</span></span>      |
| <span data-ttu-id="eb3a0-117">**Неправильн**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="eb3a0-118">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-118">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-119">**type**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-119">**type**</span></span>                  | <span data-ttu-id="eb3a0-120">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-120">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-121">**name**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-121">**name**</span></span>                  | <span data-ttu-id="eb3a0-122">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-122">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-123">**language**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-123">**language**</span></span>              | <span data-ttu-id="eb3a0-124">Нет</span><span class="sxs-lookup"><span data-stu-id="eb3a0-124">No</span></span>       |
|                       | <span data-ttu-id="eb3a0-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-125">**processorArchitecture**</span></span> | <span data-ttu-id="eb3a0-126">Нет</span><span class="sxs-lookup"><span data-stu-id="eb3a0-126">No</span></span>       |
|                       | <span data-ttu-id="eb3a0-127">**version**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-127">**version**</span></span>               | <span data-ttu-id="eb3a0-128">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-128">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-129">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-129">**publicKeyToken**</span></span>        | <span data-ttu-id="eb3a0-130">Нет</span><span class="sxs-lookup"><span data-stu-id="eb3a0-130">No</span></span>       |
| <span data-ttu-id="eb3a0-131">**зависимостей**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-131">**dependency**</span></span>        |                           | <span data-ttu-id="eb3a0-132">Нет</span><span class="sxs-lookup"><span data-stu-id="eb3a0-132">No</span></span>       |
| <span data-ttu-id="eb3a0-133">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="eb3a0-134">Нет</span><span class="sxs-lookup"><span data-stu-id="eb3a0-134">No</span></span>       |
| <span data-ttu-id="eb3a0-135">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="eb3a0-136">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-136">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-137">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-137">**oldVersion**</span></span>            | <span data-ttu-id="eb3a0-138">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-138">Yes</span></span>      |
|                       | <span data-ttu-id="eb3a0-139">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-139">**newVersion**</span></span>            | <span data-ttu-id="eb3a0-140">Да</span><span class="sxs-lookup"><span data-stu-id="eb3a0-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="eb3a0-141">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="eb3a0-141">File Location</span></span>

<span data-ttu-id="eb3a0-142">Файлы конфигурации издателя должны быть установлены в папку WinSxS.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="eb3a0-143">Они обычно устанавливаются в виде отдельного файла, но файлы конфигурации издателя можно также включать в качестве ресурса в библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="eb3a0-144">Файл конфигурации издателя нельзя включать в качестве ресурса в EXE-файл.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="eb3a0-145">EXE-файл может включать [манифест приложения](application-manifests.md) в качестве ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="eb3a0-146">Синтаксис имени файла</span><span class="sxs-lookup"><span data-stu-id="eb3a0-146">File Name Syntax</span></span>

<span data-ttu-id="eb3a0-147">Имя файла конфигурации издателя имеет *политику* форм. *основной*. *дополнительный номер*. *AssemblyName* , где *Major* и *minor* ссылаются на основную и дополнительную части [версии сборки](assembly-versions.md) , которая затронута.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="eb3a0-148">*AssemblyName* ссылается на имя сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="eb3a0-149">Например, файл конфигурации издателя для сборки Microsoft. Windows. Common-Controls версии 6,0 будет иметь следующее имя:</span><span class="sxs-lookup"><span data-stu-id="eb3a0-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="eb3a0-150">Policy. 6.0. Microsoft. Windows. Common-Controls</span><span class="sxs-lookup"><span data-stu-id="eb3a0-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="eb3a0-151">Не используйте файлы конфигурации политики для увеличения основной или вспомогательной версии сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="eb3a0-152">Например, не следует перенаправлять версию 6.0.0.0 в 7.0.0.0 или 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="eb3a0-153">Если приложение ссылается на версию сборки, например 6.0.0.0, параллельные проверки наличия файлов конфигурации политик с указанными основной и дополнительной версиями, например 6,0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="eb3a0-154">Затем приложение перенаправляется в другую версию сборки, например 6.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="eb3a0-155">Если файл конфигурации издателя увеличивает основную или дополнительную версию сборки, при последующем перенаправлении сборки может потребоваться выдача нескольких файлов конфигурации политики.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="eb3a0-156">Элементы</span><span class="sxs-lookup"><span data-stu-id="eb3a0-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="eb3a0-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**сборок**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="eb3a0-158">Элемент контейнера.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-158">A container element.</span></span> <span data-ttu-id="eb3a0-159">Его первым подэлементом должен быть **assemblyIdentity**.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="eb3a0-160">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-160">Required.</span></span>

<span data-ttu-id="eb3a0-161">Элемент Assembly должен находиться в пространстве имен **urn: schemas-microsoft-com: ASM. v1**.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="eb3a0-162">Дочерние элементы сборки также должны находиться в этом пространстве имен путем наследования или добавления тегов.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="eb3a0-163">Элемент **Assembly** имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="eb3a0-164">attribute</span><span class="sxs-lookup"><span data-stu-id="eb3a0-164">Attribute</span></span>           | <span data-ttu-id="eb3a0-165">Описание</span><span class="sxs-lookup"><span data-stu-id="eb3a0-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="eb3a0-166">**манифестверсион**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-166">**manifestVersion**</span></span> | <span data-ttu-id="eb3a0-167">Атрибут **манифестверсион** должен иметь значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="eb3a0-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**Неправильн**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="eb3a0-169">Описывает и однозначно определяет параллельную сборку.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="eb3a0-170">Как первый подэлемент элемента **Assembly** , **assemblyIdentity** описывает параллельную сборку, которая имеет одну или несколько измененных зависимостей сборок.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="eb3a0-171">Файл конфигурации издателя перенаправляет зависимости указанной сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="eb3a0-172">Например, следующий **assemblyIdentity** означает, что файл конфигурации издателя влияет на зависимости сборки x86 Microsoft. Windows. POP 6.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="eb3a0-173">Как первый подэлемент элемента **dependentAssembly** , **assemblyIdentity** описывает параллельную зависимость сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="eb3a0-174">Файл конфигурации издателя перестраивает удостоверение этой требуемой параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="eb3a0-175">Изменение задается в **bindingRedirect**.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="eb3a0-176">Например, следующий **assemblyIdentity** изменяет любую зависимость от Microsoft. Windows. самплеассембли версии 2.0.0.0 на зависимость от Microsoft. Windows. самплеассембли версии 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="eb3a0-177">Элемент **assemblyIdentity** имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="eb3a0-178">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-178">It has no sub-elements.</span></span>



| <span data-ttu-id="eb3a0-179">attribute</span><span class="sxs-lookup"><span data-stu-id="eb3a0-179">Attribute</span></span>                 | <span data-ttu-id="eb3a0-180">Описание</span><span class="sxs-lookup"><span data-stu-id="eb3a0-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3a0-181">**type**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-181">**type**</span></span>                  | <span data-ttu-id="eb3a0-182">Указывает тип сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-182">Specifies the assembly type.</span></span> <span data-ttu-id="eb3a0-183">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-183">Required.</span></span> <span data-ttu-id="eb3a0-184">На **теге assemblyIdentity** для затронутой сборки значение атрибута **Type** должно быть равно Win32-Policy.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="eb3a0-185">Значение параметра Win32-Policy должно быть не длиннее строчных букв.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="eb3a0-186">В **теге assemblyIdentity** для изменяемой зависимости сборки значение атрибута **Type** должно быть равно Win32.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="eb3a0-187">Значение Win32 должно состоять из всех строчных букв.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="eb3a0-188">**name**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-188">**name**</span></span>                  | <span data-ttu-id="eb3a0-189">Уникально именует сборку.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-189">Uniquely names an assembly.</span></span> <span data-ttu-id="eb3a0-190">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-190">Required.</span></span> <span data-ttu-id="eb3a0-191">В **теге assemblyIdentity** для затронутой сборки имя имеет *политику* формы. *основной*. *дополнительный номер*. *AssemblyName* , где *Major* и *minor* ссылаются на основную и дополнительную части [версии сборки](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="eb3a0-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="eb3a0-192">В **теге assemblyIdentity** для изменяемой зависимости сборки имя имеет форму Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="eb3a0-193">Например, Microsoft. Windows. Мисамплеапп.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="eb3a0-194">**language**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-194">**language**</span></span>              | <span data-ttu-id="eb3a0-195">Определяет язык сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="eb3a0-196">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-196">Optional.</span></span> <span data-ttu-id="eb3a0-197">В **теге assemblyIdentity** для затронутой сборки, если сборка зависит от языка, укажите код языка DHTML.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="eb3a0-198">Если сборка предназначена для использования в разных странах мира (не зависит от языка), пропустите этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="eb3a0-199">В **теге assemblyIdentity** для изменяемой зависимости сборки, если сборка зависит от языка, укажите код языка DHTML.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="eb3a0-200">Если сборка предназначена для использования в разных странах мира (не зависит от языка), задайте значение как " \* ".</span><span class="sxs-lookup"><span data-stu-id="eb3a0-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="eb3a0-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-201">**processorArchitecture**</span></span> | <span data-ttu-id="eb3a0-202">Указывает процессор, на котором работает приложение.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="eb3a0-203">**version**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-203">**version**</span></span>               | <span data-ttu-id="eb3a0-204">Указывает версию сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-204">Specifies the assembly version.</span></span> <span data-ttu-id="eb3a0-205">Используйте синтаксис версии из четырех частей: MMMM. nnnn. УУ. пппп</span><span class="sxs-lookup"><span data-stu-id="eb3a0-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="eb3a0-206">Требуется только в **теге**"DEF-контекст".</span><span class="sxs-lookup"><span data-stu-id="eb3a0-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="eb3a0-207">Не указывайте атрибут Version в **ТЕГЕ** ref-context.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="eb3a0-208">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-208">**publicKeyToken**</span></span>        | <span data-ttu-id="eb3a0-209">16-символьная шестнадцатеричная строка, представляющая последние 8 байт хэша SHA-1 открытого ключа, для которого подписана сборка.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="eb3a0-210">Открытый ключ, используемый для подписи каталога, должен иметь длину 2048 бит или более.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="eb3a0-211">Для всех общих параллельных сборок требуется publicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="eb3a0-212">Значение publicKeyToken, используемое для файла конфигурации издателя, должно совпадать с ключом, используемым для подписанной сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="eb3a0-213">Файлы конфигурации издателя можно подписывать с помощью тех же средств, которые используются со сборками. см. [пример подписывания сборки](assembly-signing-example.md) и [Создание подписанных файлов и каталогов](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="eb3a0-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="eb3a0-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**зависимостей**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="eb3a0-215">Необязательный элемент контейнера по крайней мере для одного элемента **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="eb3a0-216">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="eb3a0-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="eb3a0-218">Каждое **dependentAssembly** должно находиться внутри только одной **зависимости**.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="eb3a0-219">У **dependentAssembly** нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="eb3a0-220">Первый подэлемент **dependentAssembly** должен быть **assemblyIdentity** для параллельной сборки, перенастраиваемой конфигурацией издателя.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="eb3a0-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="eb3a0-222">Элемент **bindingRedirect** содержит сведения о перенаправлении для привязки сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="eb3a0-223">Этот элемент содержит атрибуты, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="eb3a0-224">attribute</span><span class="sxs-lookup"><span data-stu-id="eb3a0-224">Attribute</span></span>      | <span data-ttu-id="eb3a0-225">Описание</span><span class="sxs-lookup"><span data-stu-id="eb3a0-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3a0-226">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-226">**oldVersion**</span></span> | <span data-ttu-id="eb3a0-227">Указывает версию сборки, переопределяемую и перенаправляемую.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="eb3a0-228">Используйте синтаксис nnnnn. nnnnn. nnnnn. nnnnn из четырех частей.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="eb3a0-229">Укажите диапазон версий на тире без пробелов.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="eb3a0-230">Например, 2.14.3.0 или 2.14.3.0 2.16.0.0.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="eb3a0-231">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-231">Required.</span></span> |
| <span data-ttu-id="eb3a0-232">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="eb3a0-232">**newVersion**</span></span> | <span data-ttu-id="eb3a0-233">Указывает заменяющую версию сборки.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="eb3a0-234">Используйте синтаксис nnnnn. nnnnn. nnnnn. nnnnn из четырех частей.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb3a0-235">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb3a0-235">Remarks</span></span>

<span data-ttu-id="eb3a0-236">Файлы конфигурации издателя не указывают файлы.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="eb3a0-237">Обратите внимание, что файлы политики для конкретного языка отделены от файла конфигурации издателя.</span><span class="sxs-lookup"><span data-stu-id="eb3a0-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="eb3a0-238">Пример</span><span class="sxs-lookup"><span data-stu-id="eb3a0-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




