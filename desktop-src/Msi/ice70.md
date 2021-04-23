---
description: ICE70 проверяет правильность указанных целочисленных значений для записей реестра.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663975"
---
# <a name="ice70"></a><span data-ttu-id="b10c0-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="b10c0-103">ICE70</span></span>

<span data-ttu-id="b10c0-104">ICE70 проверяет правильность указанных целочисленных значений для записей реестра.</span><span class="sxs-lookup"><span data-stu-id="b10c0-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="b10c0-105">Значения в форме \# \# str, \# % unexpand str не проверяются.</span><span class="sxs-lookup"><span data-stu-id="b10c0-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="b10c0-106">Значения формы \# ксхекс, \# ксхекс, \# Integer и \# \[ Property \] проверяются.</span><span class="sxs-lookup"><span data-stu-id="b10c0-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="b10c0-107">В следующей таблице представлен краткий обзор.</span><span class="sxs-lookup"><span data-stu-id="b10c0-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="b10c0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b10c0-108">Value</span></span>                 | <span data-ttu-id="b10c0-109">Проверка</span><span class="sxs-lookup"><span data-stu-id="b10c0-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="b10c0-110">\#\#str</span><span class="sxs-lookup"><span data-stu-id="b10c0-110">\#\#str</span></span>               | <span data-ttu-id="b10c0-111">допустимым</span><span class="sxs-lookup"><span data-stu-id="b10c0-111">valid</span></span>                                                                         |
| <span data-ttu-id="b10c0-112">\#% нераскрытной str</span><span class="sxs-lookup"><span data-stu-id="b10c0-112">\#%unexpanded str</span></span>     | <span data-ttu-id="b10c0-113">допустимым</span><span class="sxs-lookup"><span data-stu-id="b10c0-113">valid</span></span>                                                                         |
| <span data-ttu-id="b10c0-114">\#Ксхекс, \# ксхекс</span><span class="sxs-lookup"><span data-stu-id="b10c0-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="b10c0-115">Проверьте Допустимые шестнадцатеричные символы (0 – 9, a-f, A-F).</span><span class="sxs-lookup"><span data-stu-id="b10c0-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="b10c0-116">Здесь можно использовать свойства.</span><span class="sxs-lookup"><span data-stu-id="b10c0-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="b10c0-117">\#+ int, \# -int, \# int</span><span class="sxs-lookup"><span data-stu-id="b10c0-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="b10c0-118">Проверьте допустимые числовые символы (0-9).</span><span class="sxs-lookup"><span data-stu-id="b10c0-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="b10c0-119">Здесь можно использовать свойства.</span><span class="sxs-lookup"><span data-stu-id="b10c0-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="b10c0-120">Синтаксис для целочисленного значения, который необходимо указать в реестре, — \# целое число, где целое число является числовым.</span><span class="sxs-lookup"><span data-stu-id="b10c0-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="b10c0-121">Результат</span><span class="sxs-lookup"><span data-stu-id="b10c0-121">Result</span></span>

<span data-ttu-id="b10c0-122">ICE70 сообщает об ошибке, если целочисленные значения для записей реестра указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="b10c0-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="b10c0-123">Пример</span><span class="sxs-lookup"><span data-stu-id="b10c0-123">Example</span></span>

<span data-ttu-id="b10c0-124">ICE70 сообщает о следующих ошибках в данном примере.</span><span class="sxs-lookup"><span data-stu-id="b10c0-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="b10c0-125">Чтобы устранить эту ошибку, измените значение, чтобы оно использовало все числовые символы.</span><span class="sxs-lookup"><span data-stu-id="b10c0-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="b10c0-126">Если требуется, чтобы значение было строкой, перед ним должно стоять два " \# " ( \# \# ), а не только один.</span><span class="sxs-lookup"><span data-stu-id="b10c0-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="b10c0-127">Чтобы устранить эту ошибку, допустимые шестнадцатеричные символы: 0-9, A-F и A-f.</span><span class="sxs-lookup"><span data-stu-id="b10c0-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="b10c0-128">Только эти символы могут следовать за \# x (или \# x).</span><span class="sxs-lookup"><span data-stu-id="b10c0-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="b10c0-129">[Таблица реестра](registry-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="b10c0-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="b10c0-130">Реестр</span><span class="sxs-lookup"><span data-stu-id="b10c0-130">Registry</span></span> | <span data-ttu-id="b10c0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b10c0-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="b10c0-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="b10c0-132">Reg1</span></span>     | <span data-ttu-id="b10c0-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="b10c0-133">\#12xz34</span></span> |
| <span data-ttu-id="b10c0-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="b10c0-134">Reg2</span></span>     | <span data-ttu-id="b10c0-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="b10c0-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="b10c0-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b10c0-136">Remarks</span></span>

-   <span data-ttu-id="b10c0-137">\#\[\]недопустимое MyProperty.</span><span class="sxs-lookup"><span data-stu-id="b10c0-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="b10c0-138">\#\[Недопустимое MyProperty (отсутствует закрывающая скобка).</span><span class="sxs-lookup"><span data-stu-id="b10c0-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="b10c0-139">\#\[myprop1 \] \[ myprop2 является допустимым.</span><span class="sxs-lookup"><span data-stu-id="b10c0-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="b10c0-140">(Несмотря на то, что в последнем случае отсутствует закрывающая квадратная скобка, myprop1 может вычислить значение \# str, поэтому будет использоваться \# \# str \[ myprop2, что является допустимым</span><span class="sxs-lookup"><span data-stu-id="b10c0-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="b10c0-141">\#\]\[недопустимое MyProperty</span><span class="sxs-lookup"><span data-stu-id="b10c0-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="b10c0-142">Любое внедренное свойство в строке значения не может иметь \[ \] форму $compkey, \[ \# филекэй \] или \[ ! филекэй, \] так как они не являются числовыми.</span><span class="sxs-lookup"><span data-stu-id="b10c0-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="b10c0-143">Однако существует одно исключение: \# \[ MyProperty \] \[ $compkey \] (или \[ \# филекэй \] или \[ ! филекэй \] ) является допустимым, так как, как и в предыдущем, \[ MyProperty \] может вычислять \# str.</span><span class="sxs-lookup"><span data-stu-id="b10c0-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b10c0-144">См. также</span><span class="sxs-lookup"><span data-stu-id="b10c0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b10c0-145">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="b10c0-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



