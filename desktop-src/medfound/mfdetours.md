---
description: Указывает поставщик Microsoft Media Foundation для обзора, который отслеживает вызовы API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: мфдетаурс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711274"
---
# <a name="mfdetours-element"></a>мфдетаурс, элемент

Указывает поставщик Microsoft Media Foundation для обзора, который отслеживает вызовы API Media Foundation.

## <a name="usage"></a>Использование

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Атрибуты



| attribute            | Тип             | Обязательно       | Описание                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Да<br/> | Уровень трассировки.<br/> <br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                               |
|---------------------------------------|
| [**This**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Последовательность дочерних элементов

``` syntax
keyword+
```

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                   |
|-------------------------------------------|
| [**поставщик**](providers.md)<br/> |



## <a name="element-information"></a>Сведения об элементе



|              |     |
|--------------|-----|
| Может быть пустым | Нет  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации Мфтраце](mftrace-configuration-file.md)
</dt> </dl>

 

 




