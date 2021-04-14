---
title: Ресурс ЗНАЧКа
description: Определяет точечный рисунок, определяющий форму значка, который будет использоваться для данного приложения или анимированного значка.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ЗНАЧОК меню ресурсов и других ресурсов
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533119"
---
# <a name="icon-resource"></a>Ресурс ЗНАЧКа

Определяет точечный рисунок, определяющий форму значка, который будет использоваться для данного приложения или анимированного значка.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Уникальное имя или 16-разрядное целочисленное значение без знака, идентифицирующее ресурс.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*файлов*
</dt> <dd>

Имя файла, содержащего ресурс. Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге. Путь должен представлять собой строку в кавычках.

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="remarks"></a>Комментарии

Ресурсы значков и курсоров могут содержать более одного изображения.

## <a name="examples"></a>Примеры

В следующем примере определяются два ресурса значка:

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование значков](./using-icons.md)
</dt> </dl>

 

 