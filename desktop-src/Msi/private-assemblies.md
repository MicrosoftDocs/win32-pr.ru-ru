---
description: Сборка Win32 может быть установлена как частная сборка и доступна для использования одним приложением. Закрытые сборки должны устанавливаться пакетом установщик Windows, который используется для установки или обновления приложения.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Частные сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264835"
---
# <a name="private-assemblies"></a><span data-ttu-id="3ddeb-104">Частные сборки</span><span class="sxs-lookup"><span data-stu-id="3ddeb-104">Private Assemblies</span></span>

<span data-ttu-id="3ddeb-105">Сборка Win32 может быть установлена как частная сборка и доступна для использования одним приложением.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="3ddeb-106">Закрытые сборки должны устанавливаться пакетом установщик Windows, который используется для установки или обновления приложения.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="3ddeb-107">В Windows XP закрытые сборки устанавливаются как [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="3ddeb-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="3ddeb-108">Установщик Windows устанавливает частные параллельные сборки в папку, которая является частной для приложения.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="3ddeb-109">Обычно это папка, содержащая исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="3ddeb-110">Зависимость приложения от закрытой сборки указывается в файле манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="3ddeb-111">Дополнительные сведения см. в разделе [изолированные приложения и параллельные сборки](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="3ddeb-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="3ddeb-112">В операционных системах, предшествующих Windows XP, копия закрытой сборки и локальный файл устанавливаются в личную папку для монопольного использования приложения.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="3ddeb-113">Версия сборки также глобально зарегистрирована в системе и доступна для любого приложения, которое привязывается к ней.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="3ddeb-114">Глобальная версия сборки может быть версией, установленной с приложением или более ранней версией.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="3ddeb-115">Глобальная версия определяется теми же правилами, которые используются [изолированными компонентами](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="3ddeb-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="3ddeb-116">Обратите внимание, что установщик Windows не может установить закрытую сборку в расположении с путем, содержащим более 234 символов, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="3ddeb-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
