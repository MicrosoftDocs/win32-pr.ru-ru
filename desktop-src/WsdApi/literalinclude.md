---
description: Помещает в созданный код инструкцию C или IDL include.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: Литералинклуде, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995131"
---
# <a name="literalinclude-element"></a><span data-ttu-id="21cd2-103">Литералинклуде, элемент</span><span class="sxs-lookup"><span data-stu-id="21cd2-103">literalInclude element</span></span>

<span data-ttu-id="21cd2-104">Помещает в созданный код инструкцию C или IDL include.</span><span class="sxs-lookup"><span data-stu-id="21cd2-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="21cd2-105">Использование</span><span class="sxs-lookup"><span data-stu-id="21cd2-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="21cd2-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="21cd2-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21cd2-107">attribute</span><span class="sxs-lookup"><span data-stu-id="21cd2-107">Attribute</span></span></th>
<th><span data-ttu-id="21cd2-108">Тип</span><span class="sxs-lookup"><span data-stu-id="21cd2-108">Type</span></span></th>
<th><span data-ttu-id="21cd2-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="21cd2-109">Required</span></span></th>
<th><span data-ttu-id="21cd2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="21cd2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21cd2-111"><strong>Язык</strong></span><span class="sxs-lookup"><span data-stu-id="21cd2-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="21cd2-112">Строка языка</span><span class="sxs-lookup"><span data-stu-id="21cd2-112">language string</span></span><br/></td>
<td><span data-ttu-id="21cd2-113">нет</span><span class="sxs-lookup"><span data-stu-id="21cd2-113">No</span></span><br/></td>
<td><span data-ttu-id="21cd2-114">Тип включаемого файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="21cd2-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="21cd2-115">
<dt><strong>Ц</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="21cd2-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="21cd2-116">Включите файл заголовка C.</span><span class="sxs-lookup"><span data-stu-id="21cd2-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="21cd2-117"><dt><strong>IDL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="21cd2-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="21cd2-118">Включите IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="21cd2-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cd2-119"><strong>Локальное</strong></span><span class="sxs-lookup"><span data-stu-id="21cd2-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="21cd2-120">Логический</span><span class="sxs-lookup"><span data-stu-id="21cd2-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="21cd2-121">нет</span><span class="sxs-lookup"><span data-stu-id="21cd2-121">No</span></span><br/></td>
<td><span data-ttu-id="21cd2-122">Этот атрибут используется только в том случае, если для параметра <strong>Language</strong> задано значение &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="21cd2-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="21cd2-123">
<dt><strong>Условия</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="21cd2-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="21cd2-124">Выполняет поиск именованного заголовка в текущем каталоге перед поиском в системных каталогах.</span><span class="sxs-lookup"><span data-stu-id="21cd2-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="21cd2-125"><dt><strong>IsFalse</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="21cd2-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="21cd2-126">Поиск только системных каталогов для именованного заголовка.</span><span class="sxs-lookup"><span data-stu-id="21cd2-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="21cd2-127">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="21cd2-127">Child elements</span></span>

<span data-ttu-id="21cd2-128">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="21cd2-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="21cd2-129">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="21cd2-129">Parent elements</span></span>



| <span data-ttu-id="21cd2-130">Элемент</span><span class="sxs-lookup"><span data-stu-id="21cd2-130">Element</span></span>                         | <span data-ttu-id="21cd2-131">Описание</span><span class="sxs-lookup"><span data-stu-id="21cd2-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="21cd2-132">**File**</span><span class="sxs-lookup"><span data-stu-id="21cd2-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="21cd2-133">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="21cd2-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="21cd2-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="21cd2-134">Remarks</span></span>

<span data-ttu-id="21cd2-135">В следующих примерах показан код, созданный из различных элементов **литералинклуде** .</span><span class="sxs-lookup"><span data-stu-id="21cd2-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="21cd2-136">Пример 1. создание инструкции include в C</span><span class="sxs-lookup"><span data-stu-id="21cd2-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="21cd2-137">Входной XML:</span><span class="sxs-lookup"><span data-stu-id="21cd2-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="21cd2-138">Выходной код:</span><span class="sxs-lookup"><span data-stu-id="21cd2-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="21cd2-139">Пример 2. создание инструкции include в C</span><span class="sxs-lookup"><span data-stu-id="21cd2-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="21cd2-140">Входной XML:</span><span class="sxs-lookup"><span data-stu-id="21cd2-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="21cd2-141">Выходной код:</span><span class="sxs-lookup"><span data-stu-id="21cd2-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="21cd2-142">Пример 3. создание инструкции импорта IDL</span><span class="sxs-lookup"><span data-stu-id="21cd2-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="21cd2-143">Входной XML:</span><span class="sxs-lookup"><span data-stu-id="21cd2-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="21cd2-144">Выходной код:</span><span class="sxs-lookup"><span data-stu-id="21cd2-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="21cd2-145">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="21cd2-145">Element information</span></span>



| <span data-ttu-id="21cd2-146">Метка</span><span class="sxs-lookup"><span data-stu-id="21cd2-146">Label</span></span> | <span data-ttu-id="21cd2-147">Значение</span><span class="sxs-lookup"><span data-stu-id="21cd2-147">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="21cd2-148">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="21cd2-148">Minimum supported system</span></span><br/> | <span data-ttu-id="21cd2-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21cd2-149">Windows Vista</span></span> |
| <span data-ttu-id="21cd2-150">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="21cd2-150">Can be empty</span></span>                        | <span data-ttu-id="21cd2-151">Да</span><span class="sxs-lookup"><span data-stu-id="21cd2-151">Yes</span></span>           |



 

 




