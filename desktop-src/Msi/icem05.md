---
description: ICEM05 проверяет, правильно ли связан модуль слияния с компонентами в модуле. Неправильное связывание компонента с модулем приводит к тому, что компонент будет неправильно связан с целевой базой данных.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee34dbc16b9cf3aeaa16aec9b5d62671cd51036c563bfb8561815ad3c21d0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996784"
---
# <a name="icem05"></a>ICEM05

ICEM05 проверяет, правильно ли связан модуль слияния с компонентами в модуле. Неправильное связывание компонента с модулем приводит к тому, что компонент будет неправильно связан с целевой базой данных.

Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.

## <a name="result"></a>Результат

ICEM05 отправляет сообщение об ошибке, если база данных модуля неправильно связывает компоненты и модуль.

## <a name="example"></a>Пример

ICEM05 отправляет следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[Таблица ModuleSignature](modulesignature-table.md)



| ModuleID         | Язык | Версия |
|------------------|----------|---------|
| MyModule. *GUID1* | 1033     | 1.0     |



 

[**Таблица Модулекомпонентс**](modulecomponents-table.md)



| Компонент  | ModuleID            | Язык |
|------------|---------------------|----------|
| Component1 | MyModule. *GUID1*    | 1033     |
| Component2 | Осермодуле. *GUID2* | 1033     |



 

[Таблица Component](component-table.md) (частичная)



| Компонент  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

Модуль слияния сообщает о первой ошибке, так как таблица Модулекомпонентс пытается связать компонент с другим модулем, который не является текущим модулем, указанным в таблице ModuleSignature. Чтобы устранить эту проблему, измените столбцы ModuleID и Language записи Модулекомпонентс для Component2 на значение для текущего модуля MyModule. *GUID1*.

Модуль слияния сообщает о второй ошибке, так как первая запись в таблице Модулекомпонентс пытается связать Component1 с модулем. Этот компонент не существует в таблице Component модуля слияния. Модуль может быть связан только с компонентом, который существует в модуле. Чтобы устранить эту проблему, удалите запись для несуществующего компонента.

Модуль слияния сообщает третью ошибку, так как модуль пытается добавить Component3 в целевую базу данных. Этот компонент не был связан с модулем в таблице Модулекомпонентс. Чтобы устранить эту ошибку, добавьте запись для Component3 в таблицу Модулекомпонентс.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



