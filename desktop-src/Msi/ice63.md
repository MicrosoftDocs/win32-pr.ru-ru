---
description: ICE63 проверяет правильность последовательности действия RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0de847a3b79c87b8ddc7dbaf3be64f88b9ef34df80d92737b6d9005ffdad24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142498"
---
# <a name="ice63"></a>ICE63

ICE63 проверяет правильность последовательности [действия RemoveExistingProducts](removeexistingproducts-action.md). Можно поместить действие RemoveExistingProducts:

1.  Между Инсталлвалидате и Инсталлинитиализе
2.  Сразу после Инсталлинитиализе или после Инсталлинитиализе, если действия между Инсталлинитиализе и RemoveExistingProducts не создают никаких действий скрипта.
3.  Сразу после Инсталлексекуте или Инсталлексекутеагаин и до функции InstallFinalize (такое же ограничение применяется, как и ранее).
4.  После функции InstallFinalize.

Ошибка при исправлении предупреждения или ошибки, о которой сообщило ICE63, приводит к сбою обновления.

## <a name="result"></a>Результат

ICE63 отправляет предупреждение или ошибку, если последовательность действия RemoveExistingProducts неверна.

## <a name="example"></a>Пример

ICE63 сообщает об ошибке в приведенном примере.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

Действие "Микустомактион" происходит между Инсталлинитиализе и RemoveExistingProducts. Если Микустомактион создает какие бы то ни было действия в сценарии, это вызывает проблемы в установке.

Чтобы устранить эту ошибку, убедитесь, что Микустомактион не создает никаких действий скриптов или не выполняет их повторное выполнение.

[Таблица Инсталлексекутесекуенце](installexecutesequence-table.md)



| Действие                 | Условие | Последовательность |
|------------------------|-----------|----------|
| инсталлинитиализе      |           | 1000     |
| микустомактион         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



