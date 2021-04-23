---
description: Установщик Windows могут устанавливать, удалять и обновлять сборки и сборки Win32, используемые средой CLR платформы Microsoft .NET.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662947"
---
# <a name="assemblies"></a><span data-ttu-id="c66e5-103">Сборки</span><span class="sxs-lookup"><span data-stu-id="c66e5-103">Assemblies</span></span>

<span data-ttu-id="c66e5-104">Установщик Windows могут устанавливать, удалять и обновлять сборки и сборки Win32, используемые средой CLR платформы Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="c66e5-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c66e5-105">Сборка обрабатывается установщик Windows как один компонент установщика.</span><span class="sxs-lookup"><span data-stu-id="c66e5-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="c66e5-106">Все файлы, составляющие сборку, должны содержаться в одном компоненте установщика, указанном в таблице [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c66e5-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="c66e5-107">Установщик Windows, выполняющиеся в Windows Vista и Windows XP, могут устанавливать параллельные сборки.</span><span class="sxs-lookup"><span data-stu-id="c66e5-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="c66e5-108">Параллельные сборки могут безопасно обмениваться сборками между несколькими приложениями и могут отменять негативные последствия совместного использования сборок, такие как конфликты DLL.</span><span class="sxs-lookup"><span data-stu-id="c66e5-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="c66e5-109">Вместо единственной версии сборки, которая предполагает обратную совместимость со всеми приложениями, параллельное совместное использование сборок позволяет нескольким версиям сборки COM или Win32 выполняться одновременно в системе.</span><span class="sxs-lookup"><span data-stu-id="c66e5-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="c66e5-110">Эта улучшенная возможность изолировать приложения является важной частью Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c66e5-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c66e5-111">Дополнительные сведения см. в разделе [изолированные приложения и параллельные сборки](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span><span class="sxs-lookup"><span data-stu-id="c66e5-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="c66e5-112">В следующих разделах описывается использование сборок с установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="c66e5-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="c66e5-113">Добавление сборок в пакет</span><span class="sxs-lookup"><span data-stu-id="c66e5-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="c66e5-114">Установка и удаление сборок</span><span class="sxs-lookup"><span data-stu-id="c66e5-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="c66e5-115">Обновление сборок</span><span class="sxs-lookup"><span data-stu-id="c66e5-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="c66e5-116">Режимы переустановки сборок среды CLR</span><span class="sxs-lookup"><span data-stu-id="c66e5-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="c66e5-117">Разделы реестра сборки, записанные установщик Windows</span><span class="sxs-lookup"><span data-stu-id="c66e5-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="c66e5-118">Сведения об установке приложений COM и COM+ 1,0 см. в статьях [Установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md), [Установка компонента COM в частном расположении](installing-a-com-component-to-a-private-location.md)и [Создание компонента COM в существующем пакете](make-a-com-component-in-an-existing-package-private.md).</span><span class="sxs-lookup"><span data-stu-id="c66e5-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
