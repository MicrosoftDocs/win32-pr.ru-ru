---
title: ШРИФТовый ресурс
description: Определяет файл, содержащий шрифт.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Меню ресурсов шрифтов и другие ресурсы
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf08abd68d5d99640435d355609d5647c71116f9fa29c137ba67a311d41f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235276"
---
# <a name="font-resource"></a>ШРИФТовый ресурс

Определяет файл, содержащий шрифт.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Уникальное 16-битовое целочисленное значение без знака, идентифицирующее ресурс.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*файлов*
</dt> <dd>

Имя файла, содержащего ресурс. Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге. Путь должен представлять собой строку в кавычках.

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="examples"></a>Примеры

В следующем примере определяется один ресурс шрифта:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




