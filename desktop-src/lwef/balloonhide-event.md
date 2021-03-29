---
title: Событие Баллунхиде
description: Событие Баллунхиде
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258940"
---
# <a name="balloonhide-event"></a>Событие Баллунхиде

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит при скрытии всплывающего окна символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Подагент* \_ **баллунхиде** **(ByVal** *чарактерид * *)**



| Отделение          | Описание                                                       |
|---------------|-------------------------------------------------------------------|
| *чарактерид* | Возвращает идентификатор символа, связанного со всплывающей подсказкой. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Сервер отправляет это событие только клиентам символа (приложения, которые загрузили символ), который использует всплывающую подсказку Word.

### <a name="see-also"></a>См. также:

[**Событие Баллуншов**](balloonshow-event.md)


 

 




