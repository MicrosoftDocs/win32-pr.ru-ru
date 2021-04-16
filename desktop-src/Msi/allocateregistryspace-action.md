---
description: Действие Аллокатерегистриспаце гарантирует, что объем свободного места в реестре, заданный свойством АВАИЛАБЛЕФРИРЕГ, существует в реестре.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Действие Аллокатерегистриспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662953"
---
# <a name="allocateregistryspace-action"></a><span data-ttu-id="3b5f5-103">Действие Аллокатерегистриспаце</span><span class="sxs-lookup"><span data-stu-id="3b5f5-103">AllocateRegistrySpace Action</span></span>

<span data-ttu-id="3b5f5-104">Действие Аллокатерегистриспаце гарантирует, что объем свободного места в реестре, заданный свойством [**аваилаблефрирег**](availablefreereg.md) , существует в реестре.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-104">The AllocateRegistrySpace action ensures that the amount of free registry space specified by the [**AVAILABLEFREEREG**](availablefreereg.md) property exists in the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3b5f5-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="3b5f5-105">Sequence Restrictions</span></span>

<span data-ttu-id="3b5f5-106">Действие Аллокатерегистриспаце должно быть вызвано после [инсталлинитиализе](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3b5f5-106">The AllocateRegistrySpace action must be called after [InstallInitialize](installinitialize-action.md).</span></span> <span data-ttu-id="3b5f5-107">Рекомендуется запланировать Аллокатерегистриспаце перед всеми остальными действиями, чтобы убедиться, что для продолжения достаточно места в реестре.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-107">It is advisable to schedule the AllocateRegistrySpace before all other actions to ensure there is enough registry space available to continue.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3b5f5-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="3b5f5-108">ActionData Messages</span></span>



| <span data-ttu-id="3b5f5-109">Поле</span><span class="sxs-lookup"><span data-stu-id="3b5f5-109">Field</span></span> | <span data-ttu-id="3b5f5-110">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="3b5f5-110">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="3b5f5-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3b5f5-111">\[1\]</span></span> | <span data-ttu-id="3b5f5-112">Пространство реестра, требуемое в КБ.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-112">Registry space required in KB.</span></span> |



 

 

 



