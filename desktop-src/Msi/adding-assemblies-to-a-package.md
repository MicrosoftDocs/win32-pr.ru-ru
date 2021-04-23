---
description: Установщик Windows разработчики могут использовать рекомендации в этом разделе для создания установщик Windows пакетов, содержащих сборки.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Добавление сборок в пакет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264206"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="4913b-103">Добавление сборок в пакет</span><span class="sxs-lookup"><span data-stu-id="4913b-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="4913b-104">Установщик Windows разработчики могут использовать рекомендации в этом разделе для создания установщик Windows пакетов, содержащих сборки.</span><span class="sxs-lookup"><span data-stu-id="4913b-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="4913b-105">Следующие рекомендации применимы к сборкам Win32 и сборкам, используемым средой CLR платформы Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="4913b-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="4913b-106">Компонент установщик Windows должен содержать не более одной сборки.</span><span class="sxs-lookup"><span data-stu-id="4913b-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="4913b-107">Все файлы в сборке должны находиться в одном компоненте.</span><span class="sxs-lookup"><span data-stu-id="4913b-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="4913b-108">Каждый компонент, содержащий сборку, должен иметь запись в таблице [мсиассембли](msiassembly-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4913b-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="4913b-109">Строгое имя кэша сборок для каждой сборки должно быть создано в таблице [мсиассемблинаме](msiassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4913b-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="4913b-110">При регистрации COM-взаимодействия для сборки используйте таблицу [реестра](registry-table.md) вместо таблицы [класса](class-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4913b-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="4913b-111">Сборки, имеющие одно и то же строгое имя, являются одной и той же сборкой.</span><span class="sxs-lookup"><span data-stu-id="4913b-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="4913b-112">Если одна и та же сборка устанавливается разными приложениями, компоненты, содержащие сборку, должны использовать одно и то же значение для ComponentId в таблицах [компонентов](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4913b-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="4913b-113">Объявления продуктов определяют сборки, которые могут быть установлены и использованы различными приложениями.</span><span class="sxs-lookup"><span data-stu-id="4913b-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="4913b-114">В объявлениях продуктов не определены закрытые сборки.</span><span class="sxs-lookup"><span data-stu-id="4913b-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="4913b-115">Добавление сборок Win32</span><span class="sxs-lookup"><span data-stu-id="4913b-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="4913b-116">При включении сборок Win32 используйте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="4913b-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="4913b-117">Значение ключевого пути в таблице [Component](component-table.md) для компонента, содержащего сборку Win32, не должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4913b-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="4913b-118">Значение ключевого пути в таблице [Component](component-table.md) для компонента, содержащего сборку политики Win32, должно быть файлом манифеста.</span><span class="sxs-lookup"><span data-stu-id="4913b-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="4913b-119">Значение ключевого пути в таблице [Component](component-table.md) для компонента, содержащего сборку Win32, которая не является сборкой политики, не должна быть файлом манифеста или каталогом.</span><span class="sxs-lookup"><span data-stu-id="4913b-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="4913b-120">Он должен быть другим файлом в сборке.</span><span class="sxs-lookup"><span data-stu-id="4913b-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="4913b-121">Добавьте строку в таблицу [мсиассемблинаме](msiassemblyname-table.md) для каждой пары "имя-значение", которая указана в разделе **assemblyIdentity** манифеста сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="4913b-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="4913b-122">Добавление сборок, используемых с платформа .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4913b-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="4913b-123">При включении сборок, используемых платформа .NET Framework среды CLR, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="4913b-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="4913b-124">Значение ключевого пути в таблице [Component](component-table.md) для компонента, содержащего сборку, не должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4913b-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="4913b-125">При установке сборки, используемой средой CLR, в глобальный кэш сборок, значение в \_ столбце Application File таблицы мсиассембли должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="4913b-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="4913b-126">Добавьте строку в таблицу [мсиассемблинаме](msiassemblyname-table.md) для каждого атрибута строгого имени сборки.</span><span class="sxs-lookup"><span data-stu-id="4913b-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="4913b-127">Все сборки должны иметь имя, версию и атрибуты языка и региональных параметров, указанные в таблице Мсиассемблинаме.</span><span class="sxs-lookup"><span data-stu-id="4913b-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="4913b-128">Для глобальной сборки требуется атрибут publicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="4913b-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="4913b-129">В следующей таблице приведен пример таблицы Мсиассемблинаме для глобальной сборки, используемой средой CLR.</span><span class="sxs-lookup"><span data-stu-id="4913b-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="4913b-130">Таблица Мсиассемблинаме</span><span class="sxs-lookup"><span data-stu-id="4913b-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="4913b-131">Компонент</span><span class="sxs-lookup"><span data-stu-id="4913b-131">Component</span></span>  | <span data-ttu-id="4913b-132">Имя</span><span class="sxs-lookup"><span data-stu-id="4913b-132">Name</span></span>           | <span data-ttu-id="4913b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4913b-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="4913b-134">Компонент а</span><span class="sxs-lookup"><span data-stu-id="4913b-134">ComponentA</span></span> | <span data-ttu-id="4913b-135">Имя</span><span class="sxs-lookup"><span data-stu-id="4913b-135">Name</span></span>           | <span data-ttu-id="4913b-136">простой</span><span class="sxs-lookup"><span data-stu-id="4913b-136">simple</span></span>           |
| <span data-ttu-id="4913b-137">Компонент а</span><span class="sxs-lookup"><span data-stu-id="4913b-137">ComponentA</span></span> | <span data-ttu-id="4913b-138">version</span><span class="sxs-lookup"><span data-stu-id="4913b-138">version</span></span>        | <span data-ttu-id="4913b-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="4913b-139">1.0.0.0</span></span>          |
| <span data-ttu-id="4913b-140">Компонент а</span><span class="sxs-lookup"><span data-stu-id="4913b-140">ComponentA</span></span> | <span data-ttu-id="4913b-141">culture</span><span class="sxs-lookup"><span data-stu-id="4913b-141">Culture</span></span>        | <span data-ttu-id="4913b-142">нейтральная тональность</span><span class="sxs-lookup"><span data-stu-id="4913b-142">neutral</span></span>          |
| <span data-ttu-id="4913b-143">Компонент а</span><span class="sxs-lookup"><span data-stu-id="4913b-143">ComponentA</span></span> | <span data-ttu-id="4913b-144">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="4913b-144">publicKeyToken</span></span> | <span data-ttu-id="4913b-145">9d1ec8380f483f5a</span><span class="sxs-lookup"><span data-stu-id="4913b-145">9d1ec8380f483f5a</span></span> |



 

 

 



