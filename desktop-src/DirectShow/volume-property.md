---
description: Свойство Volume задает или получает громкость динамика для выходных данных аудиопотока.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Свойство Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c7ebd89b971e8a8f934608ff38dc741c0db91ac2d25f717d7354b3d6294b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632884"
---
# <a name="volume-property"></a>Свойство Volume

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`Volume`Свойство задает или получает громкость динамика для выходных данных аудиопотока.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает уровень громкости в виде затухания в децибел в виде целого числа.

## <a name="remarks"></a>Remarks

Это свойство доступно для чтения и записи со значением по умолчанию 0. Полный том равен 0, а 10 000 — тишина; шкала является логарифмической. Умножьте требуемый уровень шкала на 100 (например, 10 000 = 100 dB).

 

 



