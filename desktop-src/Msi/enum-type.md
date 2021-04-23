---
description: Тип перечисления семантического типа является одним из типов текстовых форматов.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Тип перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991580"
---
# <a name="enum-type"></a><span data-ttu-id="9076b-103">Тип перечисления</span><span class="sxs-lookup"><span data-stu-id="9076b-103">Enum Type</span></span>

<span data-ttu-id="9076b-104">Тип перечисления [семантического типа](semantic-types.md) является одним из [типов текстовых форматов](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="9076b-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="9076b-105">Этот тип состоит из текстовой строки, выбранной пользователем из набора вариантов.</span><span class="sxs-lookup"><span data-stu-id="9076b-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="9076b-106">Средство слияния подставляет выбранную строку в шаблоны, указанные в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="9076b-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="9076b-107">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя текстовой строки в столбец Name, ввести "0" в столбец Format, ввести "enum" в столбец Type и ввести список возможных строк в столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="9076b-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="9076b-108">Список возможных строк должен быть указан в виде списка строк, делиминатед точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="9076b-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="9076b-109">Каждый вариант должен иметь вид "имя = значение".</span><span class="sxs-lookup"><span data-stu-id="9076b-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="9076b-110">Литеральная точка с запятой может быть добавлена к значению путем добавления символа обратной косой черты с точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="9076b-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="9076b-111">Значение null является допустимым, если только Мсмконфигитемноннуллабле не включен в поле Attributes таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="9076b-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



