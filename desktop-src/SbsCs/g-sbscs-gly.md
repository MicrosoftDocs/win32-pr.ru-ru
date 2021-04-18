---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: G (изолированные приложения и параллельные сборки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650507"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="1279a-103">G (изолированные приложения и параллельные сборки)</span><span class="sxs-lookup"><span data-stu-id="1279a-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="1279a-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G р [. J K](i-sbscs-gly.md) L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="1279a-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1279a-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**Глобальная конфигурация приложения**</span><span class="sxs-lookup"><span data-stu-id="1279a-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="1279a-106">Спецификация того, что все приложения в системе используют одинаковую параллельную версию сборки.</span><span class="sxs-lookup"><span data-stu-id="1279a-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="1279a-107">Глобальная конфигурация указывается для отдельных сборок в файле манифеста глобальной сборки, установленном в папке WinSxS.</span><span class="sxs-lookup"><span data-stu-id="1279a-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="1279a-108">Глобальная конфигурация может использоваться, когда разработчику или администратору сборки необходимо настроить все приложения в системе для использования более новой версии сборки.</span><span class="sxs-lookup"><span data-stu-id="1279a-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="1279a-109">В этом случае новая сборка должна быть обратно совместима.</span><span class="sxs-lookup"><span data-stu-id="1279a-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="1279a-110">Конфигурация для каждого приложения переопределяет конфигурацию по умолчанию или глобальные приложения для конкретных приложений.</span><span class="sxs-lookup"><span data-stu-id="1279a-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="1279a-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**Глобальный манифест сборки**</span><span class="sxs-lookup"><span data-stu-id="1279a-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="1279a-112">Файл, определяющий конфигурацию глобального приложения параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="1279a-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="1279a-113">Файлы манифеста глобальной сборки устанавливаются в системное хранилище сборок в папке WinSxS.</span><span class="sxs-lookup"><span data-stu-id="1279a-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



