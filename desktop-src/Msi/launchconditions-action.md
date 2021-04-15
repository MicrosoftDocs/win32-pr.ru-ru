---
description: Действие Лаунчкондитионс запрашивает таблицу Лаунчкондитион и вычисляет каждый условный оператор, записанный там. Если какие-либо из этих условных инструкций завершаются неудачей, пользователю выводится сообщение об ошибке и установка завершается.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Действие Лаунчкондитионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682708"
---
# <a name="launchconditions-action"></a><span data-ttu-id="e4cc4-104">Действие Лаунчкондитионс</span><span class="sxs-lookup"><span data-stu-id="e4cc4-104">LaunchConditions Action</span></span>

<span data-ttu-id="e4cc4-105">Действие Лаунчкондитионс запрашивает [таблицу лаунчкондитион](launchcondition-table.md) и вычисляет каждый условный оператор, записанный там.</span><span class="sxs-lookup"><span data-stu-id="e4cc4-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="e4cc4-106">Если какие-либо из этих условных инструкций завершаются неудачей, пользователю выводится сообщение об ошибке и установка завершается.</span><span class="sxs-lookup"><span data-stu-id="e4cc4-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e4cc4-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="e4cc4-107">Sequence Restrictions</span></span>

<span data-ttu-id="e4cc4-108">Действие Лаунчкондитионс является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e4cc4-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="e4cc4-109">Это действие обычно является первым в последовательности, но [действие аппсеарч](appsearch-action.md) может быть упорядочено до действия лаунчкондитионс.</span><span class="sxs-lookup"><span data-stu-id="e4cc4-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="e4cc4-110">Если имеются условия запуска, которые не применяются ко всем режимам установки, соответствующее свойство режима установки должно использоваться в условном выражении в соответствующей таблице последовательностей.</span><span class="sxs-lookup"><span data-stu-id="e4cc4-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e4cc4-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="e4cc4-111">ActionData Messages</span></span>

<span data-ttu-id="e4cc4-112">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="e4cc4-112">There are no ActionData messages.</span></span>

 

 



