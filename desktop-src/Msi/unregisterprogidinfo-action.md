---
description: Действие Унрегистерпрогидинфо управляет отменой регистрации данных OLE ProgId в системе.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Действие Унрегистерпрогидинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786964"
---
# <a name="unregisterprogidinfo-action"></a>Действие Унрегистерпрогидинфо

Действие Унрегистерпрогидинфо управляет отменой регистрации данных OLE ProgId в системе.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Унрегистерпрогидинфо должно следовать после действия [инсталлинитиализе](installinitialize-action.md) , [Унрегистерклассинфо](unregisterclassinfo-action.md) действия, [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) действия и перед действием [RegisterProgIdInfo](registerprogidinfo-action.md) .

[Ремоверегистривалуес](removeregistryvalues-action.md) должен предшествовать унрегистерпрогидинфо в последовательности.

Последовательность действий в следующей группе ограничена. Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.

-   [унрегистерклассинфо](unregisterclassinfo-action.md)
-   [унрегистерекстенсионинфо](unregisterextensioninfo-action.md)
-   унрегистерпрогидинфо
-   [унрегистермимеинфо](unregistermimeinfo-action.md)
-   [регистерклассинфо](registerclassinfo-action.md)
-   [регистерекстенсионинфо](registerextensioninfo-action.md)
-   [регистерпрогидинфо](registerprogidinfo-action.md)
-   [регистермимеинфо](registermimeinfo-action.md)

Например, Унрегистерпрогидинфо должен предшествовать [унрегистермимеинфо](unregistermimeinfo-action.md) в таблице Sequence.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия                |
|-------|-------------------------------------------|
| \[1\] | Идентификатор программы зарегистрированной программы. |



 

## <a name="remarks"></a>Remarks

Действие Унрегистерпрогидинфо удаляет сведения о ProgId из реестра ([Таблица ProgID](progid-table.md)) для функций, которые подключены к сведениям о расширении ([таблице расширения](extension-table.md)) или сведениям о классе ([таблице классов](class-table.md)) и выбираются для удаления.

 

 



