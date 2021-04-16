---
description: Таблица значений — это массив, связанный со свойством с квалификаторами Value и ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Квалификаторы ValueMap и value
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702651"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="a8bf1-103">Квалификаторы ValueMap и value</span><span class="sxs-lookup"><span data-stu-id="a8bf1-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="a8bf1-104">Таблица значений — это массив, связанный со свойством с квалификаторами **value** и **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="a8bf1-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="a8bf1-105">Свойство выступает в качестве индекса в массиве, сохраняя значение, представляющее одно из значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="a8bf1-106">Используя код MOF, можно иметь следующие типы карт значений:</span><span class="sxs-lookup"><span data-stu-id="a8bf1-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="a8bf1-107">Сопоставление массива с целым числом.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="a8bf1-108">Можно определить массив с квалификатором **значения** и связать массив непосредственно с целочисленным свойством, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a8bf1-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="a8bf1-109">В этом примере значение свойства **Status** является индексом строкового массива, определенного **значением**.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="a8bf1-110">Свойство может принимать только значения, соответствующие порядковым позициям в массиве **значений** минус 1.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="a8bf1-111">Например, при установке для **состояния** значения "1" сопоставляется значение "ошибка".</span><span class="sxs-lookup"><span data-stu-id="a8bf1-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="a8bf1-112">Свойство Index может принимать только значения, соответствующие позициям в массиве **значений** .</span><span class="sxs-lookup"><span data-stu-id="a8bf1-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="a8bf1-113">Например, если массив содержит 10 записей, свойство Index может иметь историю от 0 до 9, а не 30 или 177.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="a8bf1-114">Сопоставление массива с другим массивом, сопоставленное с целым числом.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="a8bf1-115">Если вы хотите создать индекс, который не использует порядковую систему подсчета, используйте квалификатор **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="a8bf1-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="a8bf1-116">Квалификатор **ValueMap** настраивает другой массив, содержащий произвольную систему нумерации индексов, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a8bf1-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="a8bf1-117">Хотя значения **ValueMap** необходимо поместить в кавычки, WMI считает значения целыми числами.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="a8bf1-118">Таким образом, в этом примере можно задать для свойства **Status** целое число в наборе **ValueMap** : 1, 3, 99 или 0.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="a8bf1-119">WMI сопоставляет каждое целое число от порядкового номера в массиве строк **ValueMap** с соответствующей позицией в массиве **значений** .</span><span class="sxs-lookup"><span data-stu-id="a8bf1-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="a8bf1-120">Например **, значение 0** соответствует значению "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="a8bf1-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="a8bf1-121">Сопоставление массива с другим массивом, сопоставленным со строкой.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="a8bf1-122">Если вы не хотите использовать целое число для индексации массива, вместо этого можно использовать строку для хранения одного из возможных значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="a8bf1-123">Для этого необходимо определить как массив **значений** , так и элемент **ValueMap** , которые содержат строки, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a8bf1-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="a8bf1-124">При использовании строкового свойства фактически допустимые значения свойства являются записями в массиве **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="a8bf1-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="a8bf1-125">Например, можно задать для параметра **Status** значение "ОК" или "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="a8bf1-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="a8bf1-126">Приложение может использовать преимущества сопоставлений удобным способом.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="a8bf1-127">Поставщик должен применять допустимый диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8bf1-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8bf1-128">Remarks</span></span>

<span data-ttu-id="a8bf1-129">При принятии решения о том, следует ли использовать /  квалификаторы ValueMap или **BitMap** / **битвалуес** , определите, может ли любое из указанных значений выполняться параллельно.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="a8bf1-130">Если могут существовать несколько одновременных значений, необходимо использовать **BitMap** / **битвалуес**.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="a8bf1-131">Если все значения являются взаимоисключающими, следует использовать  / Квалификаторы **значения** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8bf1-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a8bf1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8bf1-133">Точечный рисунок и Битвалуес</span><span class="sxs-lookup"><span data-stu-id="a8bf1-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



