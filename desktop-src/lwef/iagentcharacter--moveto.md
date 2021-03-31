---
title: Иажентчарактер MoveTo
description: Иажентчарактер MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069879"
---
# <a name="iagentcharactermoveto"></a>Иажентчарактер:: MoveTo

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Воспроизводит связанную анимацию с **перемещаемым** состоянием и перемещает рамку символов в указанное место.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно. При возврате функции эта переменная содержит идентификатор запроса.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Координата по оси x нового положения в пикселях относительно начала координат экрана (в левом верхнем углу). Расположение символа основано на левом верхнем углу фрейма анимации.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*&*
</dt> <dd>

Координата по оси y нового положения в пикселях относительно начала координат экрана (сверху слева). Расположение символа основано на левом верхнем углу фрейма анимации.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*лспид*
</dt> <dd>

Параметр, задающий в миллисекундах скорость перемещения кадра символа. Рекомендуемое значение — 1000. При указании нуля (0) кадр перемещается без воспроизведения анимации.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*
</dt> <dd>

Адрес переменной, которая получает идентификатор запроса [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .

</dd> </dl>

При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , чтобы обеспечить доступность анимации **перемещаемого** состояния перед вызовом этого метода. Даже если анимация не загружена, сервер по-прежнему перемещает кадр.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: SetPosition**](iagentcharacter--setposition.md)


 

 