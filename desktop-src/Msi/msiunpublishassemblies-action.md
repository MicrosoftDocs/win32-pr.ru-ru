---
description: Действие Мсиунпублишассемблиес управляет объявлением сборок среды CLR и удаляемых сборок Win32.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Действие Мсиунпублишассемблиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912087"
---
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="d2eee-103">Действие Мсиунпублишассемблиес</span><span class="sxs-lookup"><span data-stu-id="d2eee-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="d2eee-104">Действие Мсиунпублишассемблиес управляет объявлением сборок среды CLR и удаляемых сборок Win32.</span><span class="sxs-lookup"><span data-stu-id="d2eee-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="d2eee-105">Действие запрашивает [таблицу мсиассембли](msiassembly-table.md) , чтобы определить, какие сборки были объявлены или установлены, удаляются из глобального кэша сборок и какие сборки содержат объявленный или установленный родительский компонент, который удаляется из расположения, изолированного для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2eee-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="d2eee-106">Дополнительные сведения см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d2eee-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="d2eee-107">В системах под управлением Windows XP и более поздних версий установщик Windows может устанавливать сборки Win32 как [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d2eee-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="d2eee-108">Дополнительные сведения см. в разделе [о изолированных приложениях и параллельных сборках](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d2eee-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d2eee-109">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d2eee-109">Sequence Restrictions</span></span>

<span data-ttu-id="d2eee-110">Действие Мсиунпублишассемблиес должно следовать после [действия инсталлинитиализе](installinitialize-action.md) в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2eee-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d2eee-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d2eee-111">ActionData Messages</span></span>



| <span data-ttu-id="d2eee-112">Поле</span><span class="sxs-lookup"><span data-stu-id="d2eee-112">Field</span></span> | <span data-ttu-id="d2eee-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="d2eee-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="d2eee-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d2eee-114">\[1\]</span></span> | <span data-ttu-id="d2eee-115">Контекст приложения.</span><span class="sxs-lookup"><span data-stu-id="d2eee-115">Application context.</span></span>       |
| <span data-ttu-id="d2eee-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d2eee-116">\[2\]</span></span> | <span data-ttu-id="d2eee-117">Имя сборки.</span><span class="sxs-lookup"><span data-stu-id="d2eee-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="d2eee-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2eee-118">Remarks</span></span>

<span data-ttu-id="d2eee-119">[Действие мсипублишассемблиес](msipublishassemblies-action.md) управляет объявлением объявляемых или установленных сборок.</span><span class="sxs-lookup"><span data-stu-id="d2eee-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
