---
description: Действие Костфинализе завершает внутренний процесс расчета стоимости установки, начатого действием Костинитиализе.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Действие Костфинализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664421"
---
# <a name="costfinalize-action"></a><span data-ttu-id="0f1f1-103">Действие Костфинализе</span><span class="sxs-lookup"><span data-stu-id="0f1f1-103">CostFinalize Action</span></span>

<span data-ttu-id="0f1f1-104">Действие Костфинализе завершает внутренний процесс [*расчета стоимости*](c-gly.md) установки, начатого действием [костинитиализе](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1f1-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0f1f1-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="0f1f1-105">Sequence Restrictions</span></span>

<span data-ttu-id="0f1f1-106">Любые стандартные или [Настраиваемые действия](custom-actions.md) , влияющие на стоимость, должны быть упорядочены перед действием [костинитиализе](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1f1-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="0f1f1-107">Вызовите действие [филекост](filecost-action.md) сразу после действия костинитиализе, а затем вызовите действие костфинализе, чтобы сделать все окончательные вычисления затрат доступными для установщика через таблицу [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1f1-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="0f1f1-108">Действие Костфинализе должно быть выполнено до запуска любой последовательности пользовательских интерфейсов, что позволяет пользователю просматривать или изменять выбор и каталоги таблиц [функций](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1f1-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0f1f1-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="0f1f1-109">ActionData Messages</span></span>

<span data-ttu-id="0f1f1-110">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="0f1f1-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f1f1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f1f1-111">Remarks</span></span>

<span data-ttu-id="0f1f1-112">Действие Костфинализе запрашивает таблицу [условий](condition-table.md) , чтобы определить, какие компоненты планируется установить.</span><span class="sxs-lookup"><span data-stu-id="0f1f1-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="0f1f1-113">Затраты выполняются для каждого компонента в таблице [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1f1-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="0f1f1-114">Действие Костфинализе также проверяет, что все целевые каталоги доступны для записи, прежде чем разрешить продолжение установки.</span><span class="sxs-lookup"><span data-stu-id="0f1f1-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="0f1f1-115">Во время [административной установки](administrative-installation.md)костфинализе устанавливает все компоненты для установки, кроме компонентов, имеющих 0 в столбце Level [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f1f1-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0f1f1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="0f1f1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f1f1-117">Стоимость файлов</span><span class="sxs-lookup"><span data-stu-id="0f1f1-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



