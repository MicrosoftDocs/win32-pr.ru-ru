---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (изолированные приложения и параллельные сборки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683336"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="529c5-103">A (изолированные приложения и параллельные сборки)</span><span class="sxs-lookup"><span data-stu-id="529c5-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="529c5-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) р [. J K](i-sbscs-gly.md) L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="529c5-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="529c5-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**контекст активации**</span><span class="sxs-lookup"><span data-stu-id="529c5-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="529c5-106">Структура данных в памяти.</span><span class="sxs-lookup"><span data-stu-id="529c5-106">A data structure in memory.</span></span> <span data-ttu-id="529c5-107">Каждый раздел этой структуры содержит метаданные для параллельных функций API.</span><span class="sxs-lookup"><span data-stu-id="529c5-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="529c5-108">Например, один раздел может иметь данные перенаправления DLL, которые используются загрузчиком DLL, а другая может иметь данные COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="529c5-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="529c5-109">Эти данные могут использоваться для перенаправления загрузки библиотеки DLL в определенную версию, создания COM-объекта или создания окна до версии, которая является наиболее совместимой для приложения.</span><span class="sxs-lookup"><span data-stu-id="529c5-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="529c5-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**Конфигурация приложения**</span><span class="sxs-lookup"><span data-stu-id="529c5-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="529c5-111">Имена и версии параллельных сборок, необходимых для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="529c5-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="529c5-112">При развертывании приложения с манифестом явно определяются зависимости от конкретных версий общих параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="529c5-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="529c5-113">По умолчанию версия сборки, указанная в манифесте, является версией, используемой при активации.</span><span class="sxs-lookup"><span data-stu-id="529c5-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="529c5-114">Глобальная конфигурация приложения задает конфигурацию всех приложений в системе.</span><span class="sxs-lookup"><span data-stu-id="529c5-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="529c5-115">Конфигурация для каждого приложения может переопределять глобальную конфигурацию приложения на основе каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="529c5-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="529c5-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**Манифест конфигурации приложения**</span><span class="sxs-lookup"><span data-stu-id="529c5-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="529c5-117">Файл, указывающий параллельные сборки, которые будут использоваться полностью или частично изолированным приложением.</span><span class="sxs-lookup"><span data-stu-id="529c5-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="529c5-118">Файлы манифеста конфигурации приложения устанавливаются в ту же папку, что и исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="529c5-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="529c5-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**манифест приложения**</span><span class="sxs-lookup"><span data-stu-id="529c5-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="529c5-120">Файл, описывающий изолированное приложение.</span><span class="sxs-lookup"><span data-stu-id="529c5-120">File that describes an isolated application.</span></span> <span data-ttu-id="529c5-121">Он задает сведения, необходимые для запуска приложения, включая зависимости от закрытых сборок, конкретные версии общих сборок и метаданных для закрытых сборок.</span><span class="sxs-lookup"><span data-stu-id="529c5-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="529c5-122">Имя файла манифеста приложения — это имя исполняемого объекта приложения, за которым следует расширение MANIFEST.</span><span class="sxs-lookup"><span data-stu-id="529c5-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="529c5-123">Например, для MySampleApp.exe файл манифеста будет MySampleApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="529c5-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="529c5-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**сборок**</span><span class="sxs-lookup"><span data-stu-id="529c5-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="529c5-125">Фундаментальный модуль для именования, привязки, управления версиями, развертывания или настройки блока программного кода.</span><span class="sxs-lookup"><span data-stu-id="529c5-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="529c5-126">Эти сборки кода могут размещаться в DLL-библиотеках или сборках COM.</span><span class="sxs-lookup"><span data-stu-id="529c5-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="529c5-127">Приложения с общей функциональностью могут выполнять общие блоки программного кода, которые называются модулями или сборками кода.</span><span class="sxs-lookup"><span data-stu-id="529c5-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="529c5-128">Инфраструктура безопасного совместного использования сборок называется параллельным совместным доступом к сборкам.</span><span class="sxs-lookup"><span data-stu-id="529c5-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="529c5-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**манифест сборки**</span><span class="sxs-lookup"><span data-stu-id="529c5-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="529c5-130">Описание параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="529c5-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="529c5-131">Он задает имя, версию, файлы, ресурсы сборки, привязку данных для элементов сборки и зависимости от других параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="529c5-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="529c5-132">Файл манифеста сборки может иметь любое допустимое имя файла, если за ним следует расширение MANIFEST.</span><span class="sxs-lookup"><span data-stu-id="529c5-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



