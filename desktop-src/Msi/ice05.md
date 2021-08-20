---
description: 'ICE05 проверяет, что определенные таблицы содержат необходимые записи. Это включает, но не ограничивается проверкой таблицы свойств на наличие обязательных свойств: ProductName, Продуктлангуаже, ProductVersion, ProductCode и manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94766ed0a311243b47c2214ea21de89576d533f0d1fa76f776dedfa3afdc7da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142562"
---
# <a name="ice05"></a>ICE05

ICE05 проверяет, что определенные таблицы содержат необходимые записи. Это включает, но не ограничивается проверкой [таблицы свойств](property-table.md) на наличие обязательных свойств: [**ProductName**](productname.md), [**продуктлангуаже**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)и [**Manufacturer**](manufacturer.md).

## <a name="result"></a>Результат

ICE05 отправляет сообщение об ошибке, если требуемая запись отсутствует.

## <a name="example"></a>Пример

В приведенном примере ICE05 сообщит, что запись "ProductVersion" является обязательной в таблице "Property".

[Таблица свойств](property-table.md) (частичная)



| Свойство                           | Значение     |
|------------------------------------|-----------|
| [**ProductName**](productname.md) | мипродукт |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



