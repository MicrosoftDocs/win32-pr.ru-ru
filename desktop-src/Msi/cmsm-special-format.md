---
description: Для некоторых значений, используемых в настраиваемых модулях слияния, требуется специальная обработка текста.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Специальный формат КМСМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263843"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="7864e-103">Специальный формат КМСМ</span><span class="sxs-lookup"><span data-stu-id="7864e-103">CMSM Special Format</span></span>

<span data-ttu-id="7864e-104">Для некоторых значений, используемых в настраиваемых модулях слияния, требуется специальная обработка текста.</span><span class="sxs-lookup"><span data-stu-id="7864e-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="7864e-105">Текстовая строка, описанная в разделе "Специальный формат КМСМ", обрабатывает точку с запятой (;) и Equals (=) являются зарезервированными символами, используемыми средством слияния клиента или Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="7864e-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="7864e-106">Специальный формат КМСМ в настоящее время используется в следующих расположениях:</span><span class="sxs-lookup"><span data-stu-id="7864e-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="7864e-107">Столбец Row [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7864e-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="7864e-108">Столбец значений [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7864e-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="7864e-109">Столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md) , когда битовое значение является значением в столбце Format.</span><span class="sxs-lookup"><span data-stu-id="7864e-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="7864e-110">Столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md) , когда Text — это значение в столбце Format, а ENUM — это значение в столбце Type.</span><span class="sxs-lookup"><span data-stu-id="7864e-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="7864e-111">Столбец DefaultValue [таблицы модулеконфигуратион](moduleconfiguration-table.md) , когда key — это значение в столбце Format.</span><span class="sxs-lookup"><span data-stu-id="7864e-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="7864e-112">Настраиваемые элементы в формате ключа, используемом [**методом провидетекстдата**](configuremodule-providetextdata.md).</span><span class="sxs-lookup"><span data-stu-id="7864e-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="7864e-113">Чтобы ввести литеральные точки с запятой или равные символы в значение в специальном формате КМСМ, добавьте перед символом символ обратной косой черты (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="7864e-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="7864e-114">Литеральная обратная косая черта может быть представлена двумя символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="7864e-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="7864e-115">Один символ, префикс одной обратной косой чертой, преобразуется в один символ, даже если escape-символ не требуется.</span><span class="sxs-lookup"><span data-stu-id="7864e-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="7864e-116">Если символ точки с запятой или знака равенства не является префиксом обратной косой черты, но не имеет определенного поведения в контексте значения, результирующая строка не определена.</span><span class="sxs-lookup"><span data-stu-id="7864e-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="7864e-117">Например, столбец DefaultValue таблицы Модулеконфигуратион находится в особом формате КМСМ для всех ключевых элементов, так как символ точки с запятой является разделителем столбцов.</span><span class="sxs-lookup"><span data-stu-id="7864e-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="7864e-118">Несмотря на то, что знак равенства не имеет особого смысла в этой строке, в этой строке все равно должны быть преобразованы литеральные символы.</span><span class="sxs-lookup"><span data-stu-id="7864e-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 



