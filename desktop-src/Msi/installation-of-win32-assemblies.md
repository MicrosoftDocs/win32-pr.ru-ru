---
description: Установите сборки Win32, сделав их компонентом пакета Microsoft установщик Windows, который устанавливает или обновляет приложение.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Установка сборок Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650618"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="e2db8-103">Установка сборок Win32</span><span class="sxs-lookup"><span data-stu-id="e2db8-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="e2db8-104">Установите сборки Win32, сделав их компонентом пакета Microsoft установщик Windows, который устанавливает или обновляет приложение.</span><span class="sxs-lookup"><span data-stu-id="e2db8-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="e2db8-105">При создании [таблицы мсиассембли](msiassembly-table.md) и [таблицы мсиассемблинаме](msiassemblyname-table.md)он определяет компонент в \_ столбце Component как сборку.</span><span class="sxs-lookup"><span data-stu-id="e2db8-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="e2db8-106">Установщик задаст свойству [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) версию файла Sxs.dll в операционных системах, которые могут поддерживать сборки Win32, и не задавать это свойство в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e2db8-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="e2db8-107">В Windows Vista и Windows XP установщик Windows не записывает сведения о сборке в реестр.</span><span class="sxs-lookup"><span data-stu-id="e2db8-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="e2db8-108">Кроме того, можно использовать общие сборки, закрытые сборки и параллельные сборки.</span><span class="sxs-lookup"><span data-stu-id="e2db8-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="e2db8-109">Дополнительные сведения см. в разделе [Общие сборки](shared-assemblies.md), [закрытые сборки](private-assemblies.md)и [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e2db8-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="e2db8-110">В следующих разделах описано, как создать пакет установщик Windows для установки сборок Win32 как общего, частного или параллельного использования в различных операционных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="e2db8-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="e2db8-111">Установка сборок Win32 для параллельного совместного использования в Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2db8-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="e2db8-112">Установка сборок Win32 для закрытого использования приложения в Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2db8-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



