---
description: ICEM04 проверяет, что необходимые пустые таблицы модуля слияния пусты. Сбой исправления ошибки, ICEM04 отчеты, может привести к неправильному объединению модуля слияния.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8388cbccd576b89a70716dd7c2ca6c82ac49fb30c8c39776904753de00b68dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050164"
---
# <a name="icem04"></a>ICEM04

ICEM04 проверяет, что необходимые пустые таблицы модуля слияния пусты. Сбой исправления ошибки, ICEM04 отчеты, может привести к неправильному объединению модуля слияния.

## <a name="result"></a>Результат

ICEM04 отправляет сообщение об ошибке, если требуемые пустые таблицы модуля слияния не пусты.

## <a name="example"></a>Пример

ICEM04 отправляет следующие сообщения об ошибках для модуля, содержащего отображаемые записи базы данных.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

В следующей таблице показана частичная [Таблица адвтексекутесекуенце](advtexecutesequence-table.md).



| Действие         | Последовательность |
|----------------|----------|
| костинитиализе | 1        |



 

В следующем списке показано частичное содержимое установочного модуля:

-   модулеинсталлексекутесекуенце
-   модулеадвтексекутесекуенце
-   инсталлуисекуенце

В следующем примере показана Другая возможная ошибка.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Если модуль слияния содержит таблицу последовательности модулей, она должна содержать соответствующую пустую таблицу, независимо от того, пуста ли таблица последовательности модуля. Например, если модуль слияния содержит [таблицу модулеадминексекутесекуенце](moduleadminexecutesequence-table.md), она также должна содержать пустую таблицу админексекутесекуенце.

[Таблица феатурекомпонентс](featurecomponents-table.md) является обязательной во всех модулях слияния и должна быть пустой.

В следующей процедуре показано, как исправить ошибки.

**Устранение ошибок**

1.  Добавьте пустую [таблицу феатурекомпонентс](featurecomponents-table.md) в модуль слияния.
2.  Добавьте пустую [таблицу инсталлексекутесекуенце](installexecutesequence-table.md) в модуль слияния.
3.  Удалите действие "Костинитиализе" из [таблицы адвтексекутесекуенце](advtexecutesequence-table.md).
    > [!Note]  
    > Эта таблица должна быть пустой в модуле слияния. Действия должны присутствовать только в таблице Модулеадвтексекутесекуенце.

     

## <a name="tables-used-during-execution"></a>Таблицы, используемые во время выполнения

В следующем списке указаны таблицы, используемые во время выполнения.

-   [Таблица Феатурекомпонентс](featurecomponents-table.md)
-   \*Таблицы последовательностей модулей и соответствующие \* таблицы последовательностей.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О модулях слияния](about-merge-modules.md)
</dt> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



