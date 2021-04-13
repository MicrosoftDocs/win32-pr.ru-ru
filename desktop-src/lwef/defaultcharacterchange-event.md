---
title: Событие Дефаултчарактерчанже
description: Событие Дефаултчарактерчанже
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411144"
---
# <a name="defaultcharacterchange-event"></a>Событие Дефаултчарактерчанже

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит, когда пользователь изменяет символ по умолчанию.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Подагент. * * * дефаултчарактерчанже* *  **(ByVal** *GUID * * *)**



| Отделение   | Описание                                      |
|--------|--------------------------------------------------|
| *GUID* | Возвращает уникальный идентификатор для символа. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Это событие указывает, что пользователь изменил символ, назначенный в качестве символа по умолчанию для пользователя. Сервер отправляет его только клиентам, которые загрузили символ по умолчанию.

Когда появляется новый символ, он предполагает тот же размер, что и любой уже загруженный экземпляр символа или предыдущий символ по умолчанию (в указанном порядке).

### <a name="see-also"></a>См. также:

[**Метод шовдефаултчарактерпропертиес**](showdefaultcharacterproperties-method.md), [ **метод Load**](load-method.md)


 

 




