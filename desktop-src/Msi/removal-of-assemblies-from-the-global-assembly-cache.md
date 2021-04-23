---
description: Установщик Windows определяет, разрешено ли удаление сборки среды CLR на основе списка клиентов, независимо от сборки.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Удаление сборок из глобального кэша сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264512"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="d82c8-103">Удаление сборок из глобального кэша сборок</span><span class="sxs-lookup"><span data-stu-id="d82c8-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="d82c8-104">Установщик Windows определяет, разрешено ли удаление сборки среды CLR на основе списка клиентов, независимо от сборки.</span><span class="sxs-lookup"><span data-stu-id="d82c8-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="d82c8-105">Установщик Windows сохраняет один бит ПИН-кода для представления клиентов сборки установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d82c8-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="d82c8-106">Установщик закрепляет сборку для первого клиента установщик Windows и открепляет его при удалении последнего установщик Windows клиента.</span><span class="sxs-lookup"><span data-stu-id="d82c8-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="d82c8-107">Сборка поддерживает бит ПИН-кода для каждого клиента сборки.</span><span class="sxs-lookup"><span data-stu-id="d82c8-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="d82c8-108">Установщик Windows напрямую не несет ответственности за физическое удаление сборок среды CLR с компьютера.</span><span class="sxs-lookup"><span data-stu-id="d82c8-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="d82c8-109">Установщик отменяет закрепление сборки при удалении последнего установщик Windows клиента.</span><span class="sxs-lookup"><span data-stu-id="d82c8-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="d82c8-110">Если установщик Windows является последним клиентом сборки, среда CLR предоставляет возможность принудительной выполнения синхронной очистки сборки.</span><span class="sxs-lookup"><span data-stu-id="d82c8-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="d82c8-111">Процесс очистки является атомарным, и на этом этапе не выполняется "откат".</span><span class="sxs-lookup"><span data-stu-id="d82c8-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="d82c8-112">Все незакрепленные сборки среды CLR должны быть выполнены после того, как пользователь сможет отменить установку или удаление.</span><span class="sxs-lookup"><span data-stu-id="d82c8-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



