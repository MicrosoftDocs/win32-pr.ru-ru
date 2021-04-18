---
description: В следующей процедуре описывается установка параллельных сборок в качестве общих сборок.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Установка параллельных сборок в качестве общих сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497235"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="31273-103">Установка параллельных сборок в качестве общих сборок</span><span class="sxs-lookup"><span data-stu-id="31273-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="31273-104">В следующей процедуре описывается установка [параллельных сборок](about-side-by-side-assemblies-.md) в качестве [общих сборок](/windows/desktop/Msi/shared-assemblies).</span><span class="sxs-lookup"><span data-stu-id="31273-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="31273-105">**Установка параллельной сборки в качестве общей сборки**</span><span class="sxs-lookup"><span data-stu-id="31273-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="31273-106">Подпишите и создайте каталог для файлов в сборке.</span><span class="sxs-lookup"><span data-stu-id="31273-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="31273-107">Файлы должны быть подписаны, чтобы установить их как параллельные сборки.</span><span class="sxs-lookup"><span data-stu-id="31273-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="31273-108">Дополнительные сведения см. в разделе [Создание подписанных файлов и каталогов](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="31273-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="31273-109">Общие параллельные сборки следует устанавливать как компоненты пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="31273-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="31273-110">Это может быть тот же пакет установки, который используется для установки или обновления приложения.</span><span class="sxs-lookup"><span data-stu-id="31273-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="31273-111">Если общая сборка поставляется в составе нескольких приложений, необходимо предоставить модуль слияния, который можно включить в пакеты установки этих приложений, и создать каталог для файлов в сборке.</span><span class="sxs-lookup"><span data-stu-id="31273-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="31273-112">Для установки сборок требуется установщик Windows версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="31273-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="31273-113">Дополнительные сведения см. в разделе [установщик Windows](../msi/windows-installer-portal.md) SDK и разделах раздела [Установка сборок Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="31273-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
