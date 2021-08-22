---
title: Иажентнотифисинк перемещение
description: Иажентнотифисинк перемещение
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f32df3058a5b5c8e0a4e02a98f9a97afdbff56f349a63fceb5d70a9001391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105185"
---
# <a name="iagentnotifysinkmove"></a>Иажентнотифисинк:: Move

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Уведомляет клиентское приложение, когда символ был перемещен.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

Идентификатор перемещенного символа.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Координата по оси x нового положения в пикселях относительно начала координат экрана (в левом верхнем углу). Расположение символа основано на левом верхнем углу фрейма анимации.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*&*
</dt> <dd>

Координата по оси y нового положения в пикселях относительно начала координат экрана (сверху слева). Расположение символа основано на левом верхнем углу фрейма анимации.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*двкаусе*
</dt> <dd>

Причина перемещения символа. Параметр может быть одним из следующих:



| Значение                                                          | Описание                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const без знака Short** **невермовед = 0;**<br/>        | Символ не был перемещен.                                                        |
| **const без знака Short** **усермовед = 1;**<br/>         | Пользователь переместил символ.                                                          |
| **const без знака Short** **программовед = 2;**<br/>      | Приложение переместило символ.                                                |
| **const без знака Short** **осерпрограммовед = 3;**<br/> | Символ был перемещен другим приложением.                                             |
| **const без знака Short** **системмовед = 4**<br/>        | Сервер переместил символ, чтобы он оставался на экране после изменения разрешения экрана. |



 

</dd> </dl>

Это событие отправляется всем клиентам символа.

## <a name="see-also"></a>См. также

[**Иажентчарактер:: жетмовекаусе**](iagentcharacter--getmovecause.md), [ **иажентчарактер:: MoveTo**](iagentcharacter--moveto.md)


 

 





