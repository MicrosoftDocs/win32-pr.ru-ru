---
description: Параллельные сборки используются со следующими типами манифестов и файлов конфигурации. Манифесты и конфигурации — это XML-файлы.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Справочник по файлам манифеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144506"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="6994c-104">Справочник по файлам манифеста</span><span class="sxs-lookup"><span data-stu-id="6994c-104">Manifest Files Reference</span></span>

<span data-ttu-id="6994c-105">Параллельные сборки используются со следующими типами манифестов и файлов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6994c-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="6994c-106">Манифесты и конфигурации — это XML-файлы.</span><span class="sxs-lookup"><span data-stu-id="6994c-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="6994c-107">манифеста</span><span class="sxs-lookup"><span data-stu-id="6994c-107">Manifest</span></span>                                                               | <span data-ttu-id="6994c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6994c-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6994c-109">Манифесты сборки</span><span class="sxs-lookup"><span data-stu-id="6994c-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="6994c-110">Описывает имена, версии, ресурсы и зависимости сборок параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="6994c-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="6994c-111">Манифесты приложений</span><span class="sxs-lookup"><span data-stu-id="6994c-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="6994c-112">Описывает имена и версии общих параллельных сборок, с которыми приложение должно выполнять привязку во время выполнения, а также может содержать метаданные для частных параллельных сборок, используемых приложением.</span><span class="sxs-lookup"><span data-stu-id="6994c-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="6994c-113">Файлы конфигурации приложений</span><span class="sxs-lookup"><span data-stu-id="6994c-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="6994c-114">Перенаправляет версии сборки зависимостей сборок, используя [конфигурацию для каждого приложения](per-application-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="6994c-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="6994c-115">Файлы конфигурации издателя</span><span class="sxs-lookup"><span data-stu-id="6994c-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="6994c-116">Перенаправляет версии сборки зависимостей сборок на основе каждой сборки, используя [конфигурацию издателя](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="6994c-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="6994c-117">Список схемы файла манифеста см. в разделе [Схема файла манифеста](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6994c-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="6994c-118">Список схемы файла конфигурации приложения см. в разделе [Схема файла конфигурации приложения](application-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6994c-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="6994c-119">Список схемы файла конфигурации издателя см. в разделе [Схема файла конфигурации издателя](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6994c-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="6994c-120">Другие технологии расширяют формат, используемый версиями Windows и манифестами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6994c-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="6994c-121">Разработчики должны обратиться к документации, относящейся к используемой технологии, для получения сведений о формате манифеста.</span><span class="sxs-lookup"><span data-stu-id="6994c-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="6994c-122">Пример:</span><span class="sxs-lookup"><span data-stu-id="6994c-122">For example:</span></span>

-   [<span data-ttu-id="6994c-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="6994c-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="6994c-124">Общеязыковая среда выполнения</span><span class="sxs-lookup"><span data-stu-id="6994c-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="6994c-125">[Контроль учетных записей (UAC)](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6994c-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 
