---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (изолированные приложения и параллельные сборки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423626"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="10c47-103">P (изолированные приложения и параллельные сборки)</span><span class="sxs-lookup"><span data-stu-id="10c47-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="10c47-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) р [. J K](i-sbscs-gly.md) L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="10c47-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="10c47-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**Конфигурация для каждого приложения**</span><span class="sxs-lookup"><span data-stu-id="10c47-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="10c47-106">Конфигурация, которая может переопределять глобальную конфигурацию приложения конкретной сборки.</span><span class="sxs-lookup"><span data-stu-id="10c47-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="10c47-107">Конфигурация для каждого приложения указывается файлом манифеста конфигурации приложения, установленным в той же папке, что и исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="10c47-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="10c47-108">В файле манифеста описывается версия или диапазон версий параллельных сборок, которые будут использоваться приложением.</span><span class="sxs-lookup"><span data-stu-id="10c47-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="10c47-109">Конфигурация для каждого приложения может использоваться, когда новая версия сборки несовместима с приложением.</span><span class="sxs-lookup"><span data-stu-id="10c47-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="10c47-110">В этом случае можно переопределить конфигурацию приложения по умолчанию или глобально для конкретной параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="10c47-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="10c47-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**Частная параллельная сборка**</span><span class="sxs-lookup"><span data-stu-id="10c47-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="10c47-112">Частная параллельная сборка отображается только для указанного приложения.</span><span class="sxs-lookup"><span data-stu-id="10c47-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="10c47-113">Он устанавливается локально в изолированное приложение, а код сборки становится закрытым для контекста приложения.</span><span class="sxs-lookup"><span data-stu-id="10c47-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="10c47-114">Зависимости частной параллельной сборки описаны в файле манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="10c47-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="10c47-115">Закрытые параллельные сборки могут использоваться для смещения негативных последствий совместного использования сборок, таких как конфликты DLL, и для упрощения развертывания приложений.</span><span class="sxs-lookup"><span data-stu-id="10c47-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="10c47-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**токен открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="10c47-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="10c47-117">16-символьная шестнадцатеричная строка, представляющая последние 8 байт хэша SHA-1 открытого ключа, для которого подписана сборка.</span><span class="sxs-lookup"><span data-stu-id="10c47-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="10c47-118">Открытый ключ, используемый для подписи каталога, должен иметь длину 2048 бит или более.</span><span class="sxs-lookup"><span data-stu-id="10c47-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="10c47-119">Требуется для всех общих параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="10c47-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 



