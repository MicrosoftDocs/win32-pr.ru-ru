---
description: Действие Костинитиализе инициирует процесс расчета стоимости установки.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Действие Костинитиализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663581"
---
# <a name="costinitialize-action"></a><span data-ttu-id="cbc0a-103">Действие Костинитиализе</span><span class="sxs-lookup"><span data-stu-id="cbc0a-103">CostInitialize Action</span></span>

<span data-ttu-id="cbc0a-104">Действие Костинитиализе инициирует процесс [*расчета стоимости*](c-gly.md) установки.</span><span class="sxs-lookup"><span data-stu-id="cbc0a-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cbc0a-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="cbc0a-105">Sequence Restrictions</span></span>

<span data-ttu-id="cbc0a-106">Любые стандартные или [Настраиваемые](custom-actions.md) действия, влияющие на стоимость, должны быть упорядочены перед действием костинитиализе.</span><span class="sxs-lookup"><span data-stu-id="cbc0a-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="cbc0a-107">Вызовите действие [филекост](filecost-action.md) сразу после действия костинитиализе.</span><span class="sxs-lookup"><span data-stu-id="cbc0a-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="cbc0a-108">Затем вызовите действие [костфинализе](costfinalize-action.md) , следующее за действием костинитиализе, чтобы сделать все окончательные вычисления затрат доступными для установщика через таблицу [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc0a-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cbc0a-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="cbc0a-109">ActionData Messages</span></span>

<span data-ttu-id="cbc0a-110">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="cbc0a-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc0a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbc0a-111">Remarks</span></span>

<span data-ttu-id="cbc0a-112">Действие Костинитиализе загружает таблицу компонентов и таблицу [компонентов](feature-table.md) в память.</span><span class="sxs-lookup"><span data-stu-id="cbc0a-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="cbc0a-113">Дополнительные сведения об обработке [*затрат*](c-gly.md) в установщике см. в разделе [стоимость файлов](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="cbc0a-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbc0a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cbc0a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc0a-115">Стоимость файлов</span><span class="sxs-lookup"><span data-stu-id="cbc0a-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



