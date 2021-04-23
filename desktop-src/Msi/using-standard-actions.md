---
description: Действие выполняется в установщик Windows либо путем вызова функции Мсидоактион, либо путем включения действия в таблицу последовательности.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Использование стандартных действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650660"
---
# <a name="using-standard-actions"></a><span data-ttu-id="99f93-103">Использование стандартных действий</span><span class="sxs-lookup"><span data-stu-id="99f93-103">Using Standard Actions</span></span>

<span data-ttu-id="99f93-104">Действие выполняется в установщик Windows либо путем вызова функции [**мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) , либо путем включения действия в таблицу последовательности.</span><span class="sxs-lookup"><span data-stu-id="99f93-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="99f93-105">Поскольку большинство действий инкапсулируют одну цель, наиболее распространенным способом использования действий является упорядочивание ряда действий в последовательности для выполнения более крупной задачи.</span><span class="sxs-lookup"><span data-stu-id="99f93-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="99f93-106">В установщике есть три стандартных действия верхнего уровня, вызывающих связанный набор последовательных таблиц.</span><span class="sxs-lookup"><span data-stu-id="99f93-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="99f93-107">Эти связанные таблицы последовательностей могут содержать стандартные действия, пользовательские действия и элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="99f93-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="99f93-108">Каждое действие в таблице последовательности имеет связанный порядковый номер и может также иметь связанное условное выражение.</span><span class="sxs-lookup"><span data-stu-id="99f93-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="99f93-109">Все действия в таблице последовательностей посещаемы по порядку и выполняются только в том случае, если условное выражение имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="99f93-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="99f93-110">Хотя стандартное действие может иметь любой связанный с ним порядковый номер, многие из них имеют ограничения последовательности, которые должны быть выполнены для правильной работы действия.</span><span class="sxs-lookup"><span data-stu-id="99f93-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="99f93-111">Например, [действие филекост](filecost-action.md)должно вызываться после [действия костинитиализе](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="99f93-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="99f93-112">Дополнительные сведения об ограничениях последовательности стандартных действий см. в разделе [действия с ограничениями последовательности](actions-with-sequencing-restrictions.md), [действиями без ограничений последовательности](actions-without-sequencing-restrictions.md)или [ссылками на стандартные действия](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="99f93-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="99f93-113">В следующих разделах приводятся дополнительные сведения об использовании стандартных действий.</span><span class="sxs-lookup"><span data-stu-id="99f93-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="99f93-114">Публикация продуктов, компонентов и компонентов</span><span class="sxs-lookup"><span data-stu-id="99f93-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="99f93-115">Поиск файлов</span><span class="sxs-lookup"><span data-stu-id="99f93-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="99f93-116">Стоимость файлов</span><span class="sxs-lookup"><span data-stu-id="99f93-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="99f93-117">Установка файла</span><span class="sxs-lookup"><span data-stu-id="99f93-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="99f93-118">Изменение реестра</span><span class="sxs-lookup"><span data-stu-id="99f93-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="99f93-119">Выполняемые действия</span><span class="sxs-lookup"><span data-stu-id="99f93-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="99f93-120">См. также справочник [по стандартным действиям](about-standard-actions.md) или [стандартным](standard-actions-reference.md)действиям.</span><span class="sxs-lookup"><span data-stu-id="99f93-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



