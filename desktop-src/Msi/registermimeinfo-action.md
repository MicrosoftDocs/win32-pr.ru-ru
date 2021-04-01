---
description: Действие Регистермимеинфо регистрирует сведения о реестре, связанные с MIME, с системой.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Действие Регистермимеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813648"
---
# <a name="registermimeinfo-action"></a>Действие Регистермимеинфо

Действие Регистермимеинфо регистрирует сведения о реестре, связанные с MIME, с системой.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Регистермимеинфо должно быть получено после действия [инсталлфилес](installfiles-action.md) , действия [Унрегистермимеинфо](unregistermimeinfo-action.md) , действия [регистерклассинфо](registerclassinfo-action.md) и действия [регистерекстенсионинфо](registerextensioninfo-action.md) .

Последовательность действий в следующей группе ограничена. Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.

-   [унрегистерклассинфо](unregisterclassinfo-action.md)
-   [унрегистерекстенсионинфо](unregisterextensioninfo-action.md)
-   [унрегистерпрогидинфо](unregisterprogidinfo-action.md)
-   [унрегистермимеинфо](unregistermimeinfo-action.md)
-   [регистерклассинфо](registerclassinfo-action.md)
-   [регистерекстенсионинфо](registerextensioninfo-action.md)
-   [регистерпрогидинфо](registerprogidinfo-action.md)
-   регистермимеинфо

Например, Регистермимеинфо должен следовать после [унрегистермимеинфо](unregistermimeinfo-action.md) в таблице Sequence.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия                   |
|-------|----------------------------------------------|
| \[1\] | Идентификатор зарегистрированного типа содержимого MIME.  |
| \[2\] | Расширение, связанное с типом содержимого MIME. |



 

## <a name="remarks"></a>Комментарии

Действие Регистермимеинфо регистрирует все сведения MIME для серверов из [таблицы MIME](mime-table.md) , для которой установлен соответствующий сервер классов или сервер расширений.

 

 



