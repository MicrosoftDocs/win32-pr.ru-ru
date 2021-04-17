---
title: Ресурс КУРСОРа
description: Определяет точечный рисунок, определяющий форму курсора на экране экрана или анимированном курсоре.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Меню ресурсов КУРСОРа и другие ресурсы
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672267"
---
# <a name="cursor-resource"></a>Ресурс КУРСОРа

Определяет точечный рисунок, определяющий форму курсора на экране экрана или анимированном курсоре.

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Уникальное имя или 16-разрядное целое число без знака, определяющее ресурс.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*файлов*
</dt> <dd>

Имя файла, содержащего ресурс. Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге. Путь должен представлять собой строку в кавычках.

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="remarks"></a>Комментарии

Ресурсы значков и курсоров могут содержать более одного изображения.

## <a name="examples"></a>Примеры

В следующем примере определяются два ресурса курсора: по имени (cursor1), а другое по номеру (2):

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование курсоров](./using-cursors.md)
</dt> </dl>

 

 