---
description: Помещает в созданный код инструкцию C или IDL include.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: Литералинклуде, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702361"
---
# <a name="literalinclude-element"></a><span data-ttu-id="f8cbb-103">Литералинклуде, элемент</span><span class="sxs-lookup"><span data-stu-id="f8cbb-103">literalInclude element</span></span>

<span data-ttu-id="f8cbb-104">Помещает в созданный код инструкцию C или IDL include.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="f8cbb-105">Использование</span><span class="sxs-lookup"><span data-stu-id="f8cbb-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="f8cbb-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8cbb-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8cbb-107">attribute</span><span class="sxs-lookup"><span data-stu-id="f8cbb-107">Attribute</span></span></th>
<th><span data-ttu-id="f8cbb-108">Тип</span><span class="sxs-lookup"><span data-stu-id="f8cbb-108">Type</span></span></th>
<th><span data-ttu-id="f8cbb-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f8cbb-109">Required</span></span></th>
<th><span data-ttu-id="f8cbb-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f8cbb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8cbb-111"><strong>Язык</strong></span><span class="sxs-lookup"><span data-stu-id="f8cbb-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="f8cbb-112">Строка языка</span><span class="sxs-lookup"><span data-stu-id="f8cbb-112">language string</span></span><br/></td>
<td><span data-ttu-id="f8cbb-113">Нет</span><span class="sxs-lookup"><span data-stu-id="f8cbb-113">No</span></span><br/></td>
<td><span data-ttu-id="f8cbb-114">Тип включаемого файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="f8cbb-115">
<dt><strong>Ц</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f8cbb-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="f8cbb-116">Включите файл заголовка C.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="f8cbb-117"><dt><strong>IDL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f8cbb-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="f8cbb-118">Включите IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8cbb-119"><strong>Локальное</strong></span><span class="sxs-lookup"><span data-stu-id="f8cbb-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="f8cbb-120">Логическое</span><span class="sxs-lookup"><span data-stu-id="f8cbb-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="f8cbb-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f8cbb-121">No</span></span><br/></td>
<td><span data-ttu-id="f8cbb-122">Этот атрибут используется только в том случае, если для параметра <strong>Language</strong> задано значение &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="f8cbb-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="f8cbb-123">
<dt><strong>Условия</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f8cbb-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="f8cbb-124">Выполняет поиск именованного заголовка в текущем каталоге перед поиском в системных каталогах.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="f8cbb-125"><dt><strong>IsFalse</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f8cbb-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="f8cbb-126">Поиск только системных каталогов для именованного заголовка.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f8cbb-127">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f8cbb-127">Child elements</span></span>

<span data-ttu-id="f8cbb-128">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f8cbb-129">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f8cbb-129">Parent elements</span></span>



| <span data-ttu-id="f8cbb-130">Элемент</span><span class="sxs-lookup"><span data-stu-id="f8cbb-130">Element</span></span>                         | <span data-ttu-id="f8cbb-131">Описание</span><span class="sxs-lookup"><span data-stu-id="f8cbb-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f8cbb-132">**File**</span><span class="sxs-lookup"><span data-stu-id="f8cbb-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f8cbb-133">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f8cbb-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8cbb-134">Remarks</span></span>

<span data-ttu-id="f8cbb-135">В следующих примерах показан код, созданный из различных элементов **литералинклуде** .</span><span class="sxs-lookup"><span data-stu-id="f8cbb-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="f8cbb-136">Пример 1. создание инструкции include в C</span><span class="sxs-lookup"><span data-stu-id="f8cbb-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="f8cbb-137">Входной XML:</span><span class="sxs-lookup"><span data-stu-id="f8cbb-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="f8cbb-138">Выходной код:</span><span class="sxs-lookup"><span data-stu-id="f8cbb-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="f8cbb-139">Пример 2. создание инструкции include в C</span><span class="sxs-lookup"><span data-stu-id="f8cbb-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="f8cbb-140">Входной XML:</span><span class="sxs-lookup"><span data-stu-id="f8cbb-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="f8cbb-141">Выходной код:</span><span class="sxs-lookup"><span data-stu-id="f8cbb-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="f8cbb-142">Пример 3. создание инструкции импорта IDL</span><span class="sxs-lookup"><span data-stu-id="f8cbb-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="f8cbb-143">Входной XML:</span><span class="sxs-lookup"><span data-stu-id="f8cbb-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="f8cbb-144">Выходной код:</span><span class="sxs-lookup"><span data-stu-id="f8cbb-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="f8cbb-145">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f8cbb-145">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f8cbb-146">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="f8cbb-146">Minimum supported system</span></span><br/> | <span data-ttu-id="f8cbb-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8cbb-147">Windows Vista</span></span> |
| <span data-ttu-id="f8cbb-148">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="f8cbb-148">Can be empty</span></span>                        | <span data-ttu-id="f8cbb-149">Да</span><span class="sxs-lookup"><span data-stu-id="f8cbb-149">Yes</span></span>           |



 

 




