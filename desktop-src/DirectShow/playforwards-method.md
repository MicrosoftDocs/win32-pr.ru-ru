---
description: Метод Плайфорвардс начинает пересылать воспроизведение из текущего расположения с указанной скоростью.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Метод Плайфорвардс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806245"
---
# <a name="playforwards-method"></a>Метод Плайфорвардс

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`PlayForwards`Метод начинает пересылать воспроизведение из текущего расположения с указанной скоростью.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*нспид*
</dt> <dd>

Задает скорость воспроизведения в виде целочисленного значения. Это значение равно множителю — 1,0 — нормальная скорость воспроизведения; 2,0 — это двойная скорость, 0,5 — половина скорости и т. д. Если **нспид** не равно 1,0, звук будет выключен и подизображение будет отключено.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**плайбакквардс**](playbackwards-method.md)
</dt> </dl>

 

 



