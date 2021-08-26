---
title: Событие Дефаултчарактерчанже
description: Событие Дефаултчарактерчанже
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed166608d3f3b874e975ff58f600d24b73b50e293333b841039b2240780b4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963134"
---
# <a name="defaultcharacterchange-event"></a>Событие Дефаултчарактерчанже

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит, когда пользователь изменяет символ по умолчанию.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Подагент. * * * дефаултчарактерчанже* *  **(ByVal** *GUID * * *)**



| Часть   | Описание                                      |
|--------|--------------------------------------------------|
| *GUID* | Возвращает уникальный идентификатор для символа. |



 

</dd> </dl>

### <a name="remarks"></a>Remarks

Это событие указывает, что пользователь изменил символ, назначенный в качестве символа по умолчанию для пользователя. Сервер отправляет его только клиентам, которые загрузили символ по умолчанию.

Когда появляется новый символ, он предполагает тот же размер, что и любой уже загруженный экземпляр символа или предыдущий символ по умолчанию (в указанном порядке).

### <a name="see-also"></a>См. также:

[**Метод шовдефаултчарактерпропертиес**](showdefaultcharacterproperties-method.md), [ **метод Load**](load-method.md)


 

 




