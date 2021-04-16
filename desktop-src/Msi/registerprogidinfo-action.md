---
description: Действие Регистерпрогидинфо управляет регистрацией данных OLE ProgId в системе.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Действие Регистерпрогидинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650780"
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



 

## <a name="remarks"></a>Комментарии

Действие Регистерпрогидинфо регистрирует все сведения ProgId для серверов, указанных в [таблице ProgID](progid-table.md) , для которых был выбран соответствующий сервер классов или сервер расширений.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Таблица классов](class-table.md)
</dt> <dt>

[Таблица расширения](extension-table.md)
</dt> </dl>

 

 



