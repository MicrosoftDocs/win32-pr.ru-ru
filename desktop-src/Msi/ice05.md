---
description: 'ICE05 проверяет, что определенные таблицы содержат необходимые записи. Это включает, но не ограничивается проверкой таблицы свойств на наличие обязательных свойств: ProductName, Продуктлангуаже, ProductVersion, ProductCode и manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650935"
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



