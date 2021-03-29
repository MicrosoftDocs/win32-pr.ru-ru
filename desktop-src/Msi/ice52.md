---
description: ICE52 проверяет наличие закрытых свойств в таблице Аппсеарч. См. раздел о свойствах.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911908"
---
# <a name="ice52"></a>ICE52

ICE52 проверяет наличие закрытых свойств в [таблице аппсеарч](appsearch-table.md). См. раздел [о свойствах](about-properties.md).

При использовании Windows 2000 все свойства, заданные в столбце свойств таблицы Аппсеарч, должны быть открытыми свойствами.

## <a name="result"></a>Результат

ICE52 отправляет предупреждение, если в таблице Аппсеарч есть закрытое свойство.

## <a name="example"></a>Пример

ICE52 отправляет следующее предупреждение для приведенного примера.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[Таблица Аппсеарч](appsearch-table.md)



| Свойство  | Подпись  |
|-----------|------------|
| СВОЙСТВО1 | Signature1 |
| Свойство2 | Signature2 |



 

Чтобы устранить это предупреждение, измените пользовательское общедоступное свойство: СВОЙСТВО2.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



