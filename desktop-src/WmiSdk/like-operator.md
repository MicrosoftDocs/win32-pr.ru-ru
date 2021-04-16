---
description: Оператор LIKE определяет, соответствует ли строка символов указанному шаблону.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Оператор LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692828"
---
# <a name="like-operator"></a><span data-ttu-id="278d3-103">Оператор LIKE</span><span class="sxs-lookup"><span data-stu-id="278d3-103">LIKE Operator</span></span>

<span data-ttu-id="278d3-104">Оператор LIKE определяет, соответствует ли строка символов указанному шаблону.</span><span class="sxs-lookup"><span data-stu-id="278d3-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="278d3-105">Указанный шаблон может содержать только символы, которые должны совпадать, или содержать символы meta.</span><span class="sxs-lookup"><span data-stu-id="278d3-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="278d3-106">Фактически оператор LIKE сопоставляет подстроки с подстановочными знаками, приведенными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="278d3-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="278d3-107">Знак</span><span class="sxs-lookup"><span data-stu-id="278d3-107">Character</span></span>       | <span data-ttu-id="278d3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="278d3-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="278d3-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="278d3-109">\[ \]</span></span>           | <span data-ttu-id="278d3-110">Любой символ в указанном диапазоне ( \[ a-f \] ) или наборе ( \[ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="278d3-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="278d3-111">Любой символ, не находящиеся в диапазоне ( \[ ^ a-f \] ) или наборе ( \[ ^ abcdef \] .)</span><span class="sxs-lookup"><span data-stu-id="278d3-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="278d3-112">Любая строка из 0 (нуля) или более символов.</span><span class="sxs-lookup"><span data-stu-id="278d3-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="278d3-113">В следующем примере выполняется поиск всех экземпляров, где "Win" находится в любом месте имени класса: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="278d3-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="278d3-114">\_ подчеркивания</span><span class="sxs-lookup"><span data-stu-id="278d3-114">\_ (underscore)</span></span> | <span data-ttu-id="278d3-115">Любой символ.</span><span class="sxs-lookup"><span data-stu-id="278d3-115">Any one character.</span></span> <span data-ttu-id="278d3-116">Любой литерал, используемый в строке запроса, должен быть экранирован путем размещения внутри \[ \] (квадратных скобок).</span><span class="sxs-lookup"><span data-stu-id="278d3-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="278d3-117">Например, следующий код PowerShell извлекает все экземпляры класса **\_ операционной системы Win32** , свойство **Name** которых начинается с **FirstName**:</span><span class="sxs-lookup"><span data-stu-id="278d3-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="278d3-118">Так как символ подчеркивания является meta, если целевой объект запроса имеет символ подчеркивания, \[ \] он должен быть заключен в escape-символы "".</span><span class="sxs-lookup"><span data-stu-id="278d3-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="278d3-119">Например, можно запросить все классы, в имени которых есть двойной символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="278d3-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="278d3-120">Чтобы нахождение всех классов с двойным символом подчеркивания в имени, необходимо отменять оба символа подчеркивания на \[ \] (квадратные скобки), например:</span><span class="sxs-lookup"><span data-stu-id="278d3-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="278d3-121">Оператор LIKE можно инвертировать с помощью оператора NOT; чтобы сделать это, не забудьте поместить не непосредственно перед именем поля.</span><span class="sxs-lookup"><span data-stu-id="278d3-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="278d3-122">Пример:</span><span class="sxs-lookup"><span data-stu-id="278d3-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="278d3-123">См. также</span><span class="sxs-lookup"><span data-stu-id="278d3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="278d3-124">Операторы WQL</span><span class="sxs-lookup"><span data-stu-id="278d3-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



