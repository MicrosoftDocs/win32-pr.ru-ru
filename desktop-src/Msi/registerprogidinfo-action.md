---
description: Действие Регистерпрогидинфо управляет регистрацией данных OLE ProgId в системе.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Действие Регистерпрогидинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cebf5ddb3bf8b9c98ebea0364b685016d343afa283b937400360f31bbcebd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912834"
---
# <a name="registerprogidinfo-action"></a>Действие Регистерпрогидинфо

Действие Регистерпрогидинфо управляет регистрацией данных OLE ProgId в системе.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Регистерпрогидинфо должно быть получено после действия [инсталлфилес](installfiles-action.md) , действия [Унрегистерпрогидинфо](unregisterprogidinfo-action.md) , действия [регистерклассинфо](registerclassinfo-action.md) и действия [регистерекстенсионинфо](registerextensioninfo-action.md) .

Последовательность действий в следующей группе ограничена. Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.

-   [унрегистерклассинфо](unregisterclassinfo-action.md)
-   [унрегистерекстенсионинфо](unregisterextensioninfo-action.md)
-   [унрегистерпрогидинфо](unregisterprogidinfo-action.md)
-   [унрегистермимеинфо](unregistermimeinfo-action.md)
-   [регистерклассинфо](registerclassinfo-action.md)
-   [регистерекстенсионинфо](registerextensioninfo-action.md)
-   регистерпрогидинфо
-   [регистермимеинфо](registermimeinfo-action.md)

Например, Регистерпрогидинфо должен следовать после [регистерекстенсионинфо](registerextensioninfo-action.md) в таблице Sequence.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия                |
|-------|-------------------------------------------|
| \[1\] | Идентификатор программы зарегистрированной программы. |



 

## <a name="remarks"></a>Remarks

Действие Регистерпрогидинфо регистрирует все сведения ProgId для серверов, указанных в [таблице ProgID](progid-table.md) , для которых был выбран соответствующий сервер классов или сервер расширений.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Таблица классов](class-table.md)
</dt> <dt>

[Таблица расширения](extension-table.md)
</dt> </dl>

 

 



