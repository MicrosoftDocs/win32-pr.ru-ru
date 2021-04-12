---
description: ICE75 проверяет, что все пользовательские действия типа 17 (DLL), тип настраиваемого действия 18 (EXE), тип настраиваемого действия 21 (JScript) и настраиваемое действие типа 22 (VBScript) являются упорядоченными после действия Костфинализе.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347355"
---
# <a name="ice75"></a>ICE75

ICE75 проверяет, что все [пользовательские действия типа 17](custom-action-type-17.md) (DLL), [тип настраиваемого действия 18](custom-action-type-18.md) (exe), [тип настраиваемого действия 21](custom-action-type-21.md) (JScript) и настраиваемое [действие типа 22](custom-action-type-22.md) (VBScript) являются упорядоченными после [действия костфинализе](costfinalize-action.md). Эти типы настраиваемых действий используют в качестве источника установленный файл. ICE75 проверяет [таблицу инсталлуисекуенце](installuisequence-table.md), таблицу [инсталлексекутесекуенце](installexecutesequence-table.md), таблицу [админуисекуенце](adminuisequence-table.md)и [таблицу админексекутесекуенце](adminexecutesequence-table.md). Обратите внимание, что в этих таблицах последовательностей требуется действие Костфинализе.

## <a name="result"></a>Результат

ICE75 отправляет сообщение об ошибке, если обнаруживает пользовательское действие, используя установленный файл в качестве исходного файла, который не является последовательным после действия Костфинализе.

## <a name="example"></a>Пример

ICE75 сообщает о следующих ошибках в приведенном примере:

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[Таблица CustomAction](customaction-table.md) (частичная)



| Действие      | Тип | Источник  |
|-------------|------|---------|
| \_ФИЛИКСЕ CA | 18   | филиксе |
| \_ФИЛЕДЛЛ CA | 17   | филедлл |



 

[Таблица админуисекуенце](adminuisequence-table.md) (частичная)



| Действие      | Последовательность |
|-------------|----------|
| \_ФИЛИКСЕ CA | 1100     |



 

[Таблица админексекутесекуенце](adminexecutesequence-table.md) (частичная)



| Действие       | Последовательность |
|--------------|----------|
| \_ФИЛЕДЛЛ CA  | 800      |
| костфинализе | 1000     |



 

Чтобы устранить ошибки, поочередно Создавайте настраиваемые действия после действия Костфинализе.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



