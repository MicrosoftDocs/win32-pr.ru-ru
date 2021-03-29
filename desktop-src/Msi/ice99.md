---
description: ICE99 проверяет, что имя свойства, указанное в таблице каталога, дублирует имя, зарезервированное для открытого или закрытого использования установщик Windows.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814409"
---
# <a name="ice99"></a>ICE99

ICE99 проверяет, что имя свойства, указанное в таблице [каталога](directory-table.md) , дублирует имя, зарезервированное для открытого или закрытого использования установщик Windows.

## <a name="result"></a>Результат

ICE99 отправляет следующую ошибку.



| ICE99, ошибка                                                                                                      | Описание                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Имя каталога: 1 совпадает с \[ \] одним из открытых свойств MSI и может привести к непредвиденным побочным эффектам. | Значение в столбце Directory таблицы [Directory](directory-table.md) дублирует имя свойства, зарезервированное установщик Windows. |



 

## <a name="example"></a>Пример

ICE99 сообщает о следующей ошибке в примере:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Каталог](directory-table.md) (частичный)



| Каталог        | \_Родительский каталог | дефаултдир |
|------------------|-------------------|------------|
| CustomActionData |                   |            |



 

Чтобы исправить это предупреждение, измените имя CustomActionData.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> <dt>

[Таблица каталога](directory-table.md)
</dt> <dt>

[Не поддерживается в установщик Windows 3,0 и более ранних версиях](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



