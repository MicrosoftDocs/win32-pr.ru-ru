---
description: На следующем рисунке показано, как два приложения могут совместно использовать сборку с помощью традиционного метода совместного использования сборок.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Совместное использование сборок параллельно
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999311"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="8b2fd-103">Совместное использование сборок параллельно</span><span class="sxs-lookup"><span data-stu-id="8b2fd-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="8b2fd-104">На следующем рисунке показано, как два приложения могут совместно использовать сборку с помощью традиционного метода совместного использования сборок.</span><span class="sxs-lookup"><span data-stu-id="8b2fd-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="8b2fd-105">Проблема с традиционным совместно используемыми сборками возникает, когда приложение устанавливает версию сборки (обычно это DLL), которая не совместима с обратной совместимостью.</span><span class="sxs-lookup"><span data-stu-id="8b2fd-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="8b2fd-106">Только что установленное приложение работает, но приложения, зависящие от предыдущей версии DLL, могут перестать работать.</span><span class="sxs-lookup"><span data-stu-id="8b2fd-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![представление двух приложений, совместно использующих сборку](images/sxs1.png)

<span data-ttu-id="8b2fd-108">Изолированное приложение и параллельное решение сборки позволяют разным версиям одной и той же сборки Win32 выполняться одновременно в одной системе без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="8b2fd-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="8b2fd-109">Указав версию параллельной сборки, которую должно использовать приложение, разработчики могут гарантировать, что тестируемая конфигурация будет всегда дублироваться на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b2fd-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="8b2fd-110">Параллельное совместное использование показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8b2fd-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![реализация совместного использования сборок параллельными сборками](images/sxs2.png)

<span data-ttu-id="8b2fd-112">Дополнительные сведения см. в разделе [о изолированных приложениях и параллельных сборках](about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="8b2fd-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



