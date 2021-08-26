---
title: Размер события
description: Размер события
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146763c649ab22c59a8367e3135ee0ea277c8ae4c8e4bc58588cd70c0b5ec1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961024"
---
# <a name="size-event"></a>Размер события

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит при изменении размера символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Размер подагента* \_ **(ByVal** *чарактерид*, **ByVal** *Width*, **ByVal** *Height*)



| Часть          | Описание                                                         |
|---------------|---------------------------------------------------------------------|
| *чарактерид* | Возвращает идентификатор перемещаемого символа.                         |
| *Width*       | Возвращает новую ширину (в пикселях) символьного кадра в виде целого числа.  |
| *Height*      | Возвращает новую высоту (в пикселях) символьного кадра в виде целого числа. |



 

</dd> </dl>

### <a name="remarks"></a>Remarks

Это событие возникает, когда приложение изменяет размер символа. Это событие отправляется только клиентам символа (приложения, которые загрузили символ).

### <a name="see-also"></a>См. также:

[**Переместить событие**](move-event.md)


 

 




