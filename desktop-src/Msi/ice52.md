---
description: ICE52 проверяет наличие закрытых свойств в таблице Аппсеарч. См. раздел о свойствах.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96f514f38e44a802b092acff53ac14f10c5e5d32c03888b7d45540443d34be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044044"
---
# <a name="ice52"></a>ICE52

ICE52 проверяет наличие закрытых свойств в [таблице аппсеарч](appsearch-table.md). См. раздел [о свойствах](about-properties.md).

при использовании Windows 2000 все свойства, заданные в столбце свойств таблицы аппсеарч, должны быть открытыми свойствами.

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



