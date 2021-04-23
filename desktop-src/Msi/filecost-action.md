---
description: Филекостактион инициирует динамические действия по установке костингоф Standard.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Действие Филекост
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081643"
---
# <a name="filecost-action"></a><span data-ttu-id="c229c-103">Действие Филекост</span><span class="sxs-lookup"><span data-stu-id="c229c-103">FileCost Action</span></span>

<span data-ttu-id="c229c-104">Филекостактион инициирует динамическую [*стоимость*](c-gly.md)стандартных действий установки.</span><span class="sxs-lookup"><span data-stu-id="c229c-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c229c-105">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="c229c-105">ActionData Messages</span></span>

<span data-ttu-id="c229c-106">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="c229c-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c229c-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="c229c-107">Sequence Restrictions</span></span>

<span data-ttu-id="c229c-108">Любые стандартные или [Настраиваемые действия](custom-actions.md) , влияющие на стоимость, должны быть упорядочены перед действием [костинитиализе](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c229c-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="c229c-109">Вызовите действие Филекост сразу после действия Костинитиализе.</span><span class="sxs-lookup"><span data-stu-id="c229c-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="c229c-110">Затем вызовите действие [костфинализе](costfinalize-action.md) после действия костинитиализе, чтобы сделать все окончательные вычисления затрат доступными для установщика через таблицу [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c229c-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="c229c-111">Действие [костинитиализе](costinitialize-action.md) должно быть выполнено перед действием филекост.</span><span class="sxs-lookup"><span data-stu-id="c229c-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="c229c-112">Затем установщик определяет затраты на дисковое пространство каждого файла в таблице [файлов](file-table.md) для каждого компонента (см. [таблицу Component](component-table.md)), принимая как кластеризацию [*тома*](v-gly.md) , так и наличие существующих файлов, которые, возможно, придется перезаписывать в учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c229c-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="c229c-113">Также учитываются все действия, которые потребляют или освобождают место на диске.</span><span class="sxs-lookup"><span data-stu-id="c229c-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="c229c-114">Если найден существующий файл, выполняется проверка версии файла, чтобы определить, нужно ли устанавливать новый файл.</span><span class="sxs-lookup"><span data-stu-id="c229c-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="c229c-115">Если существующий файл имеет равный или более высокий номер версии, существующий файл не перезаписывается, а затраты на дисковое пространство не взимается.</span><span class="sxs-lookup"><span data-stu-id="c229c-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="c229c-116">Во всех случаях установщик использует результаты проверки номеров версий, чтобы задать состояние установки каждого файла.</span><span class="sxs-lookup"><span data-stu-id="c229c-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="c229c-117">Действие Филекост инициализирует вычисление затрат с помощью сеинсталлер.</span><span class="sxs-lookup"><span data-stu-id="c229c-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="c229c-118">Фактическая динамическая [*стоимость*](c-gly.md) не происходит до выполнения действия [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c229c-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c229c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c229c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c229c-120">Стоимость файлов</span><span class="sxs-lookup"><span data-stu-id="c229c-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



