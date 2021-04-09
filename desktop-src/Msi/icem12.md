---
description: ICEM12 проверяет, что в таблице Модулесекуенце стандартные действия имеют порядковые номера, а пользовательские действия имеют значения Басеактион и After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080398"
---
# <a name="icem12"></a>ICEM12

ICEM12 проверяет, что в таблице Модулесекуенце стандартные действия имеют порядковые номера, а пользовательские действия имеют значения Басеактион и After.

Этот ИЦЕМ доступен в файле Мержемод. CUB, который входит в состав пакета SDK для установщик Windows 2,0 и более поздних версий. Дополнительные сведения см. в разделе [Windows SDK компонентов для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Результат

ICEM12 отправляет сообщение об ошибке в следующих случаях:

-   Он находит, что модуль содержит [стандартное действие](standard-actions.md) без порядкового номера.
-   Он обнаруживает, что стандартное действие имеет значения, указанные в полях Басеактион или After [таблицы модулеадминуисекуенце](moduleadminuisequence-table.md), [модулеадминексекутесекуенце таблицы](moduleadminexecutesequence-table.md), таблицы [модулеадвтексекутесекуенце](moduleadvtexecutesequence-table.md), [таблицы ModuleInstallUISequence](moduleinstalluisequence-table.md)или [таблицы ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).
-   Он находит, что модуль содержит [настраиваемое действие](custom-actions.md) , не указывая значения в полях Sequence, Басеактион или After [таблицы модулеадминуисекуенце таблица](moduleadminuisequence-table.md), [Таблица модулеадминексекутесекуенце таблицы](moduleadminexecutesequence-table.md), [Таблица модулеадвтексекутесекуенце](moduleadvtexecutesequence-table.md), таблица [ModuleInstallUISequence](moduleinstalluisequence-table.md)или [Таблица ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).

ICEM12 отправляет предупреждение, если обнаруживает пользовательское действие с указанным порядковым номером, но не имеет значения в полях Басеактион и After.

Обратите внимание, что все действия, найденные в [таблице CustomAction](customaction-table.md) , считаются пользовательскими действиями. Все остальные действия считаются стандартными действиями.

## <a name="example"></a>Пример

ICEM12 отправляет следующие сообщения об ошибках и предупреждения для модуля, содержащего записи базы данных, показанные ниже:

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| Действие  | Тип | Источник  | Назначение  |
|---------|------|---------|---------|
| Action1 превышают | 30   | Источник1 | Target1 |
| Action3 | 30   | source3 | target3 |



 

[модулеадминексекутесекуенце](moduleadminexecutesequence-table.md)



| Действие  | Последовательность | басеактион | После | Условие |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1 превышают    | 1     | true      |
| Action3 |          |            |       | true      |



 

[модулеинсталлексекутесекуенце](moduleinstallexecutesequence-table.md)



| Действие  | Последовательность | басеактион | После | Условие |
|---------|----------|------------|-------|-----------|
| Action1 превышают | 1        |            |       | true      |



 

Чтобы устранить эти ошибки, попробуйте выполнить следующие действия.

-   Удалите порядковый номер для настраиваемого действия Action1 превышают и используйте вместо него поля Басеактион и After.
-   Введите значения в поля Sequence, Басеактион или After для настраиваемого действия Action3. Оставьте поля Басеактион и After пустыми для стандартного действия Action2.
-   Не оставляйте поле последовательности пустым для стандартного действия Action2.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



