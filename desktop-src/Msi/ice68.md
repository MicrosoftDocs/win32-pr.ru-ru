---
description: ICE68 проверяет, что все типы пользовательских действий, необходимые для установки, являются допустимыми.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664549"
---
# <a name="ice68"></a>ICE68

ICE68 проверяет, что все типы пользовательских действий, необходимые для установки, являются допустимыми. Ошибка исправления ошибки, о которой сообщила ICE68, приводит к сбою установки, которая пытается выполнить действие. ICE68 выдает предупреждение, если атрибут **msidbCustomActionTypeNoImpersonate** задан без установки атрибута **мсидбкустомактионтипеинскрипт** .

## <a name="result"></a>Результат

ICE68 возвращает ошибку, если тип действия, необходимый для установки, является недопустимым.

## <a name="example"></a>Пример

ICE68 отправляет следующее предупреждение, если в настраиваемом действии задан бит **msidbCustomActionTypeNoImpersonate** , установленный в поле Type таблицы CustomAction, без **мсидбкустомактионтипеинскрипт** также.

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Чтобы устранить это предупреждение, включите **мсидбкустомактионтипеинскрипт** (0x400), если настраиваемое действие содержит **msidbCustomActionTypeNoImpersonate** (0x800). В противном случае установщик игнорирует атрибут **msidbCustomActionTypeNoImpersonate** . Дополнительные сведения см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).

ICE68 сообщает об ошибке в приведенном примере:

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 не является допустимым типом действия.

Чтобы устранить эту ошибку, выберите допустимый тип настраиваемого действия.

[Таблица CustomAction](customaction-table.md) (частичная)



| Действие  | Тип | Источник   | Назначение     |
|---------|------|----------|------------|
| Action1 превышают | 1027 | Аргумент | Component1 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



