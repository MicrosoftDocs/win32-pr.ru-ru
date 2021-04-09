---
title: Размер события
description: Размер события
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888219"
---
# <a name="size-event"></a>Размер события

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит при изменении размера символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Размер подагента* \_ **(ByVal** *чарактерид*, **ByVal** *Width*, **ByVal** *Height*)



| Отделение          | Описание                                                         |
|---------------|---------------------------------------------------------------------|
| *чарактерид* | Возвращает идентификатор перемещаемого символа.                         |
| *Width*       | Возвращает новую ширину (в пикселях) символьного кадра в виде целого числа.  |
| *Height*      | Возвращает новую высоту (в пикселях) символьного кадра в виде целого числа. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Это событие возникает, когда приложение изменяет размер символа. Это событие отправляется только клиентам символа (приложения, которые загрузили символ).

### <a name="see-also"></a>См. также:

[**Переместить событие**](move-event.md)


 

 




