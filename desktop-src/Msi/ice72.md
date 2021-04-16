---
description: ICE72 проверяет, что невстроенные пользовательские действия не используются в таблице Адвтексекутесекуенце.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664267"
---
# <a name="ice72"></a>ICE72

ICE72 проверяет, что невстроенные пользовательские действия не используются в [таблице адвтексекутесекуенце](advtexecutesequence-table.md). В таблице Адвтексекутесекуенце разрешается использовать пользовательские действия Type 19, Type 35 и 51 Type. Если используются другие настраиваемые действия, объявление может работать не так, как ожидалось.

## <a name="result"></a>Результат

ICE72 возвращает ошибку, если в таблице Адвексекутесекуенце используются пользовательские действия, отличные от типов 35, Type 51 и Type 19.

## <a name="example"></a>Пример

ICE72 сообщает об ошибке в приведенном примере:

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Чтобы устранить эту ошибку, удалите "CA1" из таблицы Адвтексекутесекуенце.

[Таблица адвтексекутесекуенце](advtexecutesequence-table.md) (частичная)



| Действие |
|--------|
| CA1    |
| CA35   |



 

[Таблица CustomAction](customaction-table.md) (частичная)



| Действие | Тип |
|--------|------|
| CA1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>Таблицы, используемые во время выполнения

[Таблица Адвтексекутесекуенце](advtexecutesequence-table.md)

[Таблица CustomAction](customaction-table.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Тип настраиваемого действия 19](custom-action-type-19.md)
</dt> <dt>

[Тип настраиваемого действия 35](custom-action-type-35.md)
</dt> <dt>

[Тип настраиваемого действия 51](custom-action-type-51.md)
</dt> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



