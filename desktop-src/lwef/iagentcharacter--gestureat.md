---
title: Иажентчарактер Жестуреат
description: Иажентчарактер Жестуреат
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976454"
---
# <a name="iagentcharactergestureat"></a>Иажентчарактер:: Жестуреат

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




