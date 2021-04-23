---
description: Сборка Win32 может быть установлена как общая сборка и доступна для использования несколькими приложениями на компьютере. Общие сборки должны устанавливаться пакетом установщик Windows, который используется для установки или обновления приложения.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Общие сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815440"
---
# <a name="shared-assemblies"></a><span data-ttu-id="301a2-104">Общие сборки</span><span class="sxs-lookup"><span data-stu-id="301a2-104">Shared Assemblies</span></span>

<span data-ttu-id="301a2-105">Сборка Win32 может быть установлена как общая сборка и доступна для использования несколькими приложениями на компьютере.</span><span class="sxs-lookup"><span data-stu-id="301a2-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="301a2-106">Общие сборки должны устанавливаться пакетом установщик Windows, который используется для установки или обновления приложения.</span><span class="sxs-lookup"><span data-stu-id="301a2-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="301a2-107">Общие сборки устанавливаются как [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="301a2-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="301a2-108">Установщик Windows устанавливает общие параллельные сборки в папку WinSxS.</span><span class="sxs-lookup"><span data-stu-id="301a2-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="301a2-109">Сборки не регистрируются глобально в системе, но они глобально доступны для любого приложения, которое указывает зависимость от сборки в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="301a2-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="301a2-110">Дополнительные сведения см. в разделе [изолированные приложения и параллельные сборки](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="301a2-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="301a2-111">В операционных системах, предшествующих Windows XP, общие сборки обычно устанавливаются в системную папку Windows и регистрируются глобально.</span><span class="sxs-lookup"><span data-stu-id="301a2-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="301a2-112">Последняя установленная версия доступна для любого приложения, которое выполняет привязку к ней.</span><span class="sxs-lookup"><span data-stu-id="301a2-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="301a2-113">Сведения о создании пакета установщик Windows для установки общей сборки см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="301a2-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="301a2-114">Установка сборок Win32 для параллельного совместного использования в Windows XP</span><span class="sxs-lookup"><span data-stu-id="301a2-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="301a2-115">Установка сборок Win32 для закрытого использования приложения в Windows XP</span><span class="sxs-lookup"><span data-stu-id="301a2-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
