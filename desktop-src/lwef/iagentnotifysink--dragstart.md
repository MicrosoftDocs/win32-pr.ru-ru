---
title: Иажентнотифисинк Драгстарт
description: Иажентнотифисинк Драгстарт
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3510449923d4567d3126bf9cd84655acd782b021f9f37f655a51114122a4717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105218"
---
# <a name="iagentnotifysinkdragstart"></a>Иажентнотифисинк::D Рагстарт

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Уведомляет клиентское приложение, когда пользователь начинает перетаскивать символ.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор перетаскиваемого символа.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*
</dt> <dd>

Параметр, указывающий кнопку мыши и состояние клавиши-модификатора. Параметр может возвращать любое сочетание следующих параметров:



| Значение  | Описание      |
|--------|------------------|
| 0x0001 | Левая кнопка      |
| 0x0010 | Средняя кнопка    |
| 0x0002 | Правая кнопка     |
| 0x0004 | Shift + стрелка вниз   |
| 0x0008 | Клавиша управления |
| 0x0020 | Клавиша Alt     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*&*
</dt> <dd>

Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).

</dd> </dl>

 

 




