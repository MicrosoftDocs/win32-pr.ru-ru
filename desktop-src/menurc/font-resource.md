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
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784275"
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

 

 




