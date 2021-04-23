---
description: Действие ExecuteAction инициирует последовательность выполнения с помощью свойства EXECUTEACTION, чтобы определить, какой тип установки необходимо выполнить.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Действие ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497793"
---
# <a name="executeaction-action"></a><span data-ttu-id="d82c7-103">Действие ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="d82c7-103">ExecuteAction Action</span></span>

<span data-ttu-id="d82c7-104">Действие ExecuteAction инициирует последовательность выполнения с помощью свойства [**ExecuteAction**](executeaction.md) , чтобы определить, какой тип установки необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="d82c7-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d82c7-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d82c7-105">Sequence Restrictions</span></span>

<span data-ttu-id="d82c7-106">Это действие должно быть упорядочено после завершения всей сбора информации, необходимой для начала установки.</span><span class="sxs-lookup"><span data-stu-id="d82c7-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="d82c7-107">Дополнительные действия могут быть упорядочены после действия ExecuteAction в [таблице инсталлуисекуенце](installuisequence-table.md)и в [таблице админуисекуенце](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d82c7-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="d82c7-108">Последовательность обычно начинается с действий по [*затратам*](c-gly.md) , например [действия костинитиализе](costinitialize-action.md), за которыми следуют действия пользовательского интерфейса, а затем действие ExecuteAction.</span><span class="sxs-lookup"><span data-stu-id="d82c7-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d82c7-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d82c7-109">ActionData Messages</span></span>

<span data-ttu-id="d82c7-110">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="d82c7-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d82c7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d82c7-111">Remarks</span></span>

<span data-ttu-id="d82c7-112">Действие ExecuteAction выполняется с системными привилегиями, если служба установщика включена.</span><span class="sxs-lookup"><span data-stu-id="d82c7-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="d82c7-113">Действия верхнего уровня, такие как [действие установки](install-action.md), [действие объявления](advertise-action.md)и [Административное действие](admin-action.md) , включают внутреннюю логику, определяющую, требуется ли выполнение вызова действия ExecuteAction или последовательности выполнения или пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d82c7-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d82c7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d82c7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d82c7-115">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="d82c7-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="d82c7-116">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="d82c7-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="d82c7-117">Действие Костинитиализе</span><span class="sxs-lookup"><span data-stu-id="d82c7-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



