---
title: Ресурс HTML
description: Определяет HTML-файл.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Меню ресурсов HTML и другие ресурсы
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947feb790b5fbee628c846f88595b1ae25db4cfddedbbab223fd05513560d63e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687776"
---
# <a name="html-resource"></a>Ресурс HTML

Определяет HTML-файл.

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Уникальное имя или 16-разрядное целочисленное значение без знака, идентифицирующее ресурс.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*файлов*
</dt> <dd>

Имя HTML-файла. Он должен быть полным или относительным путем, если файл не находится в текущем рабочем каталоге. Путь должен представлять собой строку в кавычках.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере определяется ресурс HTML:

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




