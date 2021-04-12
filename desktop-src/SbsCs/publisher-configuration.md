---
description: Файл конфигурации издателя глобально перенаправляет приложения и сборки, имеющие зависимость от одной версии параллельной сборки, для использования другой версии той же сборки.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Конфигурация издателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272057"
---
# <a name="publisher-configuration"></a><span data-ttu-id="692ec-103">Конфигурация издателя</span><span class="sxs-lookup"><span data-stu-id="692ec-103">Publisher Configuration</span></span>

<span data-ttu-id="692ec-104">[Файл конфигурации издателя](publisher-configuration-files.md) глобально перенаправляет приложения и сборки, имеющие зависимость от одной версии параллельной сборки, для использования другой версии той же сборки.</span><span class="sxs-lookup"><span data-stu-id="692ec-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="692ec-105">Это позволяет приложениям и сборкам использовать обновленную сборку без перестроения всех затронутых приложений.</span><span class="sxs-lookup"><span data-stu-id="692ec-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="692ec-106">[Файлы конфигурации издателя](publisher-configuration-files.md) могут предоставляться издателем сборки при выдаче новой версии сборки с совместимыми исправлениями ошибок или обновлениями безопасности.</span><span class="sxs-lookup"><span data-stu-id="692ec-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="692ec-107">Обновленная версия должна быть полностью обратно совместима.</span><span class="sxs-lookup"><span data-stu-id="692ec-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="692ec-108">Файл конфигурации издателя никогда не должен использоваться для добавления новых функций, если только обновление не полностью обратно совместимо.</span><span class="sxs-lookup"><span data-stu-id="692ec-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="692ec-109">Файлы конфигурации издателя никогда не следует использовать для увеличения основной или дополнительной версии сборки.</span><span class="sxs-lookup"><span data-stu-id="692ec-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="692ec-110">Например, не следует перенаправлять версию сборки 6.0.0.0 в 7.0.0.0 или 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="692ec-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="692ec-111">Файлы конфигурации издателя должны выдаваться только издателем сборки.</span><span class="sxs-lookup"><span data-stu-id="692ec-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="692ec-112">Разработчики сборок должны подписывать общие параллельные сборки и файлы конфигурации издателя.</span><span class="sxs-lookup"><span data-stu-id="692ec-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="692ec-113">Используйте тот же ключ, чтобы подписать сборку и связанные файлы конфигурации издателя.</span><span class="sxs-lookup"><span data-stu-id="692ec-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="692ec-114">Файлы конфигурации издателя должны быть подписаны с помощью тех же инструментов, которые используются для сборок, см. [пример подписывания сборки](assembly-signing-example.md) и [Создание подписанных файлов и каталогов](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="692ec-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="692ec-115">Как правило, Новая версия сборки и связанный с ней файл конфигурации издателя будут установлены в пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="692ec-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="692ec-116">Файлы конфигурации издателя никогда не должны предоставляться в качестве распространяемых приложений, так как установка файла конфигурации издателя глобально перенаправляет сборки в системе.</span><span class="sxs-lookup"><span data-stu-id="692ec-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="692ec-117">Если обновляемая сборка предоставляется в качестве распространяемого пакета, издатель должен предоставить оба следующих объекта.</span><span class="sxs-lookup"><span data-stu-id="692ec-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="692ec-118">Пакет установщик Windows (MSI-файл), включающий новую версию сборки с конфигурацией издателя.</span><span class="sxs-lookup"><span data-stu-id="692ec-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="692ec-119">Он может быть установлен как пакет обновления или QFE, так как в данном случае клиент выбрал глобально обновление системы.</span><span class="sxs-lookup"><span data-stu-id="692ec-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="692ec-120">Эта версия пакета никогда не должна устанавливаться приложениями.</span><span class="sxs-lookup"><span data-stu-id="692ec-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="692ec-121">Модуль слияния установщик Windows (MSM-файл), включающий только новую версию сборки.</span><span class="sxs-lookup"><span data-stu-id="692ec-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="692ec-122">Эта версия может быть включена в приложения.</span><span class="sxs-lookup"><span data-stu-id="692ec-122">This version may be included with applications.</span></span>

<span data-ttu-id="692ec-123">Приложения, для которых требуется минимальная версия сборки, должны зависеть от минимальной версии, если минимальная версия недоступна в системе, то приложение не сможет запуститься.</span><span class="sxs-lookup"><span data-stu-id="692ec-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="692ec-124">Если он доступен в качестве распространяемого, он должен быть включен в программу установки приложения.</span><span class="sxs-lookup"><span data-stu-id="692ec-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="692ec-125">Например, при установке следующего [файла конфигурации издателя](publisher-configuration-files.md) выполняется перенаправление привязки с версии 2.0.0.0 Microsoft. Windows. самплеассембли на версию 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="692ec-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="692ec-126">При этом добавляется новая политика с именем 1.1.0.0. Policy в разделе% systemDrive% \\ Windows \\ WinSxS Policies политики \\ \\ x86 \_ Policy. 2.0. Microsoft. Windows. самплеассембли \_ 75e377300ab7b886 \_ x-WW \_ < *хашвалуе*>.</span><span class="sxs-lookup"><span data-stu-id="692ec-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="692ec-127">При установке следующего файла конфигурации издателя для той же сборки привязка перенаправления выполняется с версии 2.0.0.0 Microsoft. Windows. Самплеассембли на версию 2.0.3.0.</span><span class="sxs-lookup"><span data-stu-id="692ec-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="692ec-128">При этом добавляется другая политика с именем 2.1.0.0. Policy в разделе% systemDrive% \\ Windows \\ WinSxS \\ Policies политики \\ x86 \_ Policy. 2.0. Microsoft. Windows. самплеассембли \_ 75e377300ab7b886 \_ x-WW \_ < *хашвалуе*>.</span><span class="sxs-lookup"><span data-stu-id="692ec-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



