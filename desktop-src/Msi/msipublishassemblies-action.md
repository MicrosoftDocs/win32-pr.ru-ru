---
description: Действие Мсипублишассемблиес управляет объявлением сборок среды CLR и сборок Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Действие Мсипублишассемблиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664543"
---
# <a name="msipublishassemblies-action"></a><span data-ttu-id="adca2-103">Действие Мсипублишассемблиес</span><span class="sxs-lookup"><span data-stu-id="adca2-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="adca2-104">Действие Мсипублишассемблиес управляет объявлением сборок среды CLR и сборок Win32.</span><span class="sxs-lookup"><span data-stu-id="adca2-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="adca2-105">Действие запрашивает [таблицу мсиассембли](msiassembly-table.md) , чтобы определить, какие сборки содержат компоненты, объявляемые или установленные в глобальном кэше сборок, а также какие сборки имеют родительский компонент, объявленный или установленный в расположении, изолированном для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="adca2-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="adca2-106">Дополнительные сведения см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="adca2-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="adca2-107">В операционных системах Microsoft Windows XP и более поздних версиях установщик Windows может устанавливать сборки Win32 как [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="adca2-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="adca2-108">Дополнительные сведения см. в разделе [о изолированных приложениях и параллельных сборках](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="adca2-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="adca2-109">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="adca2-109">Sequence Restrictions</span></span>

<span data-ttu-id="adca2-110">Действие Мсипублишассемблиес должно следовать после [действия инсталлинитиализе](installinitialize-action.md) в таблице [Инсталлексекутесекуенце](installexecutesequence-table.md) или [таблице адвтексекутесекуенце](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="adca2-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="adca2-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="adca2-111">ActionData Messages</span></span>



| <span data-ttu-id="adca2-112">Поле</span><span class="sxs-lookup"><span data-stu-id="adca2-112">Field</span></span> | <span data-ttu-id="adca2-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="adca2-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="adca2-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="adca2-114">\[1\]</span></span> | <span data-ttu-id="adca2-115">Контекст приложения.</span><span class="sxs-lookup"><span data-stu-id="adca2-115">Application context.</span></span>       |
| <span data-ttu-id="adca2-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="adca2-116">\[2\]</span></span> | <span data-ttu-id="adca2-117">Имя сборки.</span><span class="sxs-lookup"><span data-stu-id="adca2-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="adca2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adca2-118">Remarks</span></span>

<span data-ttu-id="adca2-119">Дополнительные сведения см. в разделе [сборки](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="adca2-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="adca2-120">[Действие мсиунпублишассемблиес](msiunpublishassemblies-action.md) управляет объявлением удаляемых сборок.</span><span class="sxs-lookup"><span data-stu-id="adca2-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
