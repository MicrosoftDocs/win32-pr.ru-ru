---
description: Помещает в созданный код инструкцию C или IDL include.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: Литералинклуде, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcfbd72300607dd2c6f3f21e4be3666083b559cb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625320"
---
# <a name="literalinclude-element"></a>Литералинклуде, элемент

Помещает в созданный код инструкцию C или IDL include.

## <a name="usage"></a>Использование

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Язык</strong><br/></td>
<td>Строка языка<br/></td>
<td>Нет<br/></td>
<td>Тип включаемого файла заголовка. <br/> <br/>
<dt><strong>Ц</strong></dt> <dd> Включите файл заголовка C.<br/> </dd> <dt><strong>IDL</strong></dt> <dd> Включите IDL-файл.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Локальное</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Этот атрибут используется только в том случае, если для параметра <strong>Language</strong> задано значение &quot; C &quot; .<br/> <br/>
<dt><strong>Условия</strong></dt> <dd> Выполняет поиск именованного заголовка в текущем каталоге перед поиском в системных каталогах.<br/> </dd> <dt><strong>IsFalse</strong></dt> <dd> Поиск только системных каталогов для именованного заголовка.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                         | Описание                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**File**](file.md)<br/> | Выводит файл из генератора кода.<br/> <br/> |



## <a name="remarks"></a>Remarks

В следующих примерах показан код, созданный из различных элементов **литералинклуде** .

### <a name="example-1---generating-a-c-include-statement"></a>Пример 1. создание инструкции include в C

Входной XML:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Выходной код:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Пример 2. создание инструкции include в C

Входной XML:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Выходной код:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Пример 3. создание инструкции импорта IDL

Входной XML:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Выходной код:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Сведения об элементе



| Метка | Значение |
|-------------------------------------|---------------|
| Минимальная поддерживаемая система<br/> | Windows Vista |
| Может быть пустым                        | Да           |



 

 




