---
description: Свойство Фрамесперсеконд извлекает частоту кадров видео для текущего заголовка DVD.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Фрамесперсеконд, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a883f031680a57711fa092f29bc9ecbd76cb1a017c03f80337959050e62cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015672"
---
# <a name="framespersecond-property"></a>Фрамесперсеконд, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`FramesPerSecond`Свойство получает частоту кадров видео для текущего заголовка DVD.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее частоту кадров видео; 25 или 30 кадров в секунду.

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию. Видеосигналы NTSC отображаются в 30 кадров в секунду. Список PAL отображается по 25 кадров в секунду. Диск кодируется для воспроизведения на NTSC или PAL, но не может воспроизводиться одновременно.

 

 



