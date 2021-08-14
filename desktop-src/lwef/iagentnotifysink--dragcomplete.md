---
title: Иажентнотифисинк Драгкомплете
description: Иажентнотифисинк Драгкомплете
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63c24abd41f0509293ba2fafeb055f195a4d13ad354662e8d32d0fb1715e1fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477032"
---
# <a name="iagentnotifysinkdragcomplete"></a>Иажентнотифисинк::D Рагкомплете

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Уведомляет клиентское приложение, когда пользователь прекращает перетаскивание символа.

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

 

 




