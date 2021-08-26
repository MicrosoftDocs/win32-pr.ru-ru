---
description: Действие Регистермимеинфо регистрирует сведения о реестре, связанные с MIME, с системой.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Действие Регистермимеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369f35eab4e6d4228167bfbeda48cf21249ea6a63297f5a9e893b84dcc4ed5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041744"
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



 

## <a name="remarks"></a>Remarks

Действие Регистермимеинфо регистрирует все сведения MIME для серверов из [таблицы MIME](mime-table.md) , для которой установлен соответствующий сервер классов или сервер расширений.

 

 



