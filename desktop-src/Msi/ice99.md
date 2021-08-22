---
description: ICE99 проверяет, что имя свойства, указанное в таблице каталога, дублирует имя, зарезервированное для открытого или закрытого использования установщик Windows.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315274"
---
# <a name="ice99"></a>ICE99

ICE99 проверяет, что имя свойства, указанное в таблице [каталога](directory-table.md) , дублирует имя, зарезервированное для открытого или закрытого использования установщик Windows.

## <a name="result"></a>Результат

ICE99 отправляет следующую ошибку.



| ICE99, ошибка                                                                                                      | Описание                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Имя каталога: 1 совпадает с \[ \] одним из открытых свойств MSI и может привести к непредвиденным побочным эффектам. | значение в столбце directory таблицы [directory](directory-table.md) дублирует имя свойства, зарезервированное установщик Windows. |



 

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> <dt>

[Таблица каталога](directory-table.md)
</dt> <dt>

[не поддерживается в установщик Windows 3,0 и более ранних версиях](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



