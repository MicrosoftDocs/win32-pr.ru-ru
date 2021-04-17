---
description: ICE65 проверяет, что в таблице окружения отсутствуют недопустимые префиксы или значения для добавления.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651110"
---
# <a name="ice65"></a><span data-ttu-id="43a3e-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="43a3e-103">ICE65</span></span>

<span data-ttu-id="43a3e-104">ICE65 проверяет, что в [таблице окружения](environment-table.md) отсутствуют недопустимые префиксы или значения для добавления.</span><span class="sxs-lookup"><span data-stu-id="43a3e-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="43a3e-105">Ошибка исправления предупреждения или ошибки, о которой сообщает ICE65, обычно приводит к проблемам при установке, удалении или восстановлении переменной среды.</span><span class="sxs-lookup"><span data-stu-id="43a3e-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="43a3e-106">Например, можно удалить только некоторые значения определенной переменной, если одно или несколько значений для этой переменной имеют замыкающий разделитель.</span><span class="sxs-lookup"><span data-stu-id="43a3e-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="43a3e-107">Результат</span><span class="sxs-lookup"><span data-stu-id="43a3e-107">Result</span></span>

<span data-ttu-id="43a3e-108">ICE65 отправляет предупреждение или ошибку, если таблица окружения содержит недопустимые значения префикса или добавления.</span><span class="sxs-lookup"><span data-stu-id="43a3e-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="43a3e-109">Пример</span><span class="sxs-lookup"><span data-stu-id="43a3e-109">Example</span></span>

<span data-ttu-id="43a3e-110">ICE65 сообщает о следующей ошибке и предупреждении для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="43a3e-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="43a3e-111">Завершающий символ NULL в конце значения ( \[ ~ \] ) помечает это значение как добавляемое в начало любого существующего значения.</span><span class="sxs-lookup"><span data-stu-id="43a3e-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="43a3e-112">Символ, непосредственно предшествующий значению NULL (точка с запятой), становится разделителем для этого значения.</span><span class="sxs-lookup"><span data-stu-id="43a3e-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="43a3e-113">Это значение также имеет точку с запятой в начале строки.</span><span class="sxs-lookup"><span data-stu-id="43a3e-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="43a3e-114">Чтобы устранить эту ошибку, просто удалите начальную точку с запятой.</span><span class="sxs-lookup"><span data-stu-id="43a3e-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="43a3e-115">Ведущий символ NULL в значении ( \[ ~ \] ) помечает это значение как добавляемое к любому существующему значению.</span><span class="sxs-lookup"><span data-stu-id="43a3e-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="43a3e-116">Символ сразу после значения NULL становится разделителем для этого значения.</span><span class="sxs-lookup"><span data-stu-id="43a3e-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="43a3e-117">В этом случае этот символ является буквой «e», которая также происходит в середине добавляемой строки.</span><span class="sxs-lookup"><span data-stu-id="43a3e-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="43a3e-118">Это условие (наличие разделителя, совпадающего с символом в добавляемой строке) может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="43a3e-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="43a3e-119">Буква «e», которая является обычной буквой, может быть найдена в значении.</span><span class="sxs-lookup"><span data-stu-id="43a3e-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="43a3e-120">Лучшим выбором будет ";" или другой символ, не являющийся буквенно-цифровым.</span><span class="sxs-lookup"><span data-stu-id="43a3e-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="43a3e-121">(Однако если значением является путь, то ":" и " \\ " и "." являются рискованными вариантами.)</span><span class="sxs-lookup"><span data-stu-id="43a3e-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="43a3e-122">Чтобы устранить это предупреждение, используйте другой символ-разделитель.</span><span class="sxs-lookup"><span data-stu-id="43a3e-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="43a3e-123">Таблица среды</span><span class="sxs-lookup"><span data-stu-id="43a3e-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="43a3e-124">Компонент</span><span class="sxs-lookup"><span data-stu-id="43a3e-124">Component</span></span> | <span data-ttu-id="43a3e-125">Каталог</span><span class="sxs-lookup"><span data-stu-id="43a3e-125">Directory</span></span> | <span data-ttu-id="43a3e-126">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="43a3e-126">Attributes</span></span>         | <span data-ttu-id="43a3e-127">Путь</span><span class="sxs-lookup"><span data-stu-id="43a3e-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="43a3e-128">Var1</span><span class="sxs-lookup"><span data-stu-id="43a3e-128">Var1</span></span>      | <span data-ttu-id="43a3e-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="43a3e-129">TestVar</span></span>   | <span data-ttu-id="43a3e-130">\[~\]; аппендсис</span><span class="sxs-lookup"><span data-stu-id="43a3e-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="43a3e-131">тесткомпонент</span><span class="sxs-lookup"><span data-stu-id="43a3e-131">TestComponent</span></span> |
| <span data-ttu-id="43a3e-132">Var2</span><span class="sxs-lookup"><span data-stu-id="43a3e-132">Var2</span></span>      | <span data-ttu-id="43a3e-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="43a3e-133">TestVar</span></span>   | <span data-ttu-id="43a3e-134">\[~\]еаппендсис</span><span class="sxs-lookup"><span data-stu-id="43a3e-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="43a3e-135">тесткомпонент</span><span class="sxs-lookup"><span data-stu-id="43a3e-135">TestComponent</span></span> |
| <span data-ttu-id="43a3e-136">Var3</span><span class="sxs-lookup"><span data-stu-id="43a3e-136">Var3</span></span>      | <span data-ttu-id="43a3e-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="43a3e-137">TestVar</span></span>   | <span data-ttu-id="43a3e-138">; Препендсис;\[~\]</span><span class="sxs-lookup"><span data-stu-id="43a3e-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="43a3e-139">тесткомпонент</span><span class="sxs-lookup"><span data-stu-id="43a3e-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43a3e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="43a3e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a3e-141">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="43a3e-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



