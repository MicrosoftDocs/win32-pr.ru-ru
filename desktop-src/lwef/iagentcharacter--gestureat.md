---
title: Иажентчарактер Жестуреат
description: Иажентчарактер Жестуреат
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411456"
---
# <a name="iagentcharactergestureat"></a>Иажентчарактер:: Жестуреат

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Воспроизводит связанную анимацию состояния **жестуринг** на основе указанного расположения.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно. Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Координата по оси x указанного расположения в пикселях относительно начала координат экрана (в левом верхнем углу).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*&*
</dt> <dd>

Координата по оси y указанного расположения в пикселях относительно начала экрана (в левом верхнем углу).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*
</dt> <dd>

Адрес переменной, которая получает идентификатор запроса **жестуреат** .

</dd> </dl>

Сервер автоматически определяет и воспроизводит соответствующую анимацию жестуринг на основе текущей позиции символа и указанного расположения. При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](iagentcharacter--prepare.md) , чтобы убедиться, что анимации доступны перед вызовом этого метода.

 

 




