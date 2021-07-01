---
title: Иажентнотифисинк щелкните
description: Иажентнотифисинк щелкните
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120907"
---
# <a name="iagentnotifysinkclick"></a>Иажентнотифисинк:: Click

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Уведомляет клиентское приложение, когда пользователь щелкает значок символа или символа на панели задач.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор нажатого символа.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*
</dt> <dd>

Параметр, указывающий кнопку мыши и состояние клавиши-модификатора. Параметр может возвращать любое сочетание следующих параметров:



| Значение  | Описание                                    |
|--------|------------------------------------------------|
| 0x0001 | Левая кнопка                                    |
| 0x0010 | Средняя кнопка                                  |
| 0x0002 | Правая кнопка                                   |
| 0x0004 | Shift + стрелка вниз                                 |
| 0x0008 | Клавиша управления                               |
| 0x0020 | Клавиша Alt                                   |
| 0x1000 | Событие произошло на значке панели задач "символ" |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*&*
</dt> <dd>

Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).

</dd> </dl>

Это событие отправляется клиенту input-Active для символа. Если ни один из клиентов символа не является входным, сервер уведомляет об активном клиенте символа. Если символ является видимым, сервер также делает ввод клиента активным и отправляет [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md). Если символ скрыт, также автоматически отображается символ.

 

 




