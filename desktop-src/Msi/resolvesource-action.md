---
description: Действие Ресолвесаурце определяет расположение источника и задает свойство SourceDir, если источник еще не был разрешен.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Действие Ресолвесаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664263"
---
# <a name="resolvesource-action"></a><span data-ttu-id="50f66-103">Действие Ресолвесаурце</span><span class="sxs-lookup"><span data-stu-id="50f66-103">ResolveSource Action</span></span>

<span data-ttu-id="50f66-104">Действие Ресолвесаурце определяет расположение источника и задает свойство [**SourceDir**](sourcedir.md) , если источник еще не был разрешен.</span><span class="sxs-lookup"><span data-stu-id="50f66-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="50f66-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="50f66-105">Sequence Restrictions</span></span>

<span data-ttu-id="50f66-106">Действие Ресолвесаурце должно следовать после [действия костинитиализе](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="50f66-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="50f66-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="50f66-107">ActionData Messages</span></span>

<span data-ttu-id="50f66-108">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="50f66-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f66-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50f66-109">Remarks</span></span>

<span data-ttu-id="50f66-110">Действие Ресолвесаурце должно быть вызвано до использования свойства [**SourceDir**](sourcedir.md) в любом выражении.</span><span class="sxs-lookup"><span data-stu-id="50f66-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="50f66-111">Он также должен вызываться перед попыткой получить значение свойства **SourceDir** с помощью [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="50f66-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="50f66-112">Действие Ресолвесаурце не должно выполняться, если источник недоступен, так как это может быть при удалении приложения.</span><span class="sxs-lookup"><span data-stu-id="50f66-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f66-113">См. также</span><span class="sxs-lookup"><span data-stu-id="50f66-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f66-114">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="50f66-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



