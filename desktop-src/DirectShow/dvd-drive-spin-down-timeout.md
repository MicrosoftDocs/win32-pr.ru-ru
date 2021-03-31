---
description: Время ожидания вращения DVD-дисковода
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Время ожидания вращения DVD-дисковода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894958"
---
# <a name="dvd-drive-spin-down-timeout"></a>Время ожидания вращения DVD-дисковода

На переносных компьютерах, чтобы сэкономить время работы батареи, может быть желательно уменьшить продолжительность времени, в течение которого DVD-дисковод будет продолжать работать после приостановки воспроизведения пользователем. По умолчанию на DVD-диске диск вращается в течение двух минут. Это значение можно изменить в реестре Windows с помощью этого раздела:


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



where


```
Sec
```



время вращения в секундах.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Приложения](appendixes.md)
</dt> </dl>

 

 



