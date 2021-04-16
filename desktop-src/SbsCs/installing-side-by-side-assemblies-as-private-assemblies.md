---
description: Для установки параллельных сборок в качестве частных сборок можно установить сборку как компонент пакета установщика.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Установка параллельных сборок в качестве закрытых сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650506"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="350b2-103">Установка параллельных сборок в качестве закрытых сборок</span><span class="sxs-lookup"><span data-stu-id="350b2-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="350b2-104">Для установки [параллельных сборок](about-side-by-side-assemblies-.md) в качестве [частных сборок](/windows/desktop/Msi/private-assemblies)можно установить сборку как компонент пакета установщика.</span><span class="sxs-lookup"><span data-stu-id="350b2-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="350b2-105">Это может быть тот же пакет установки, который используется для установки или обновления приложения.</span><span class="sxs-lookup"><span data-stu-id="350b2-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="350b2-106">Для установки сборок требуется установщик Windows версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="350b2-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="350b2-107">Дополнительные сведения см. в разделе [установщик Windows](../msi/windows-installer-portal.md) SDK и разделах раздела [Установка сборок Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="350b2-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="350b2-108">В качестве альтернативы можно использовать установщик для копирования закрытой сборки и манифеста в ту же папку, что и исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="350b2-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
