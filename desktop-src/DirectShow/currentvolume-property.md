---
description: Свойство Куррентволуме извлекает номер тома для текущего корневого каталога.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Куррентволуме, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654607"
---
# <a name="currentvolume-property"></a>Куррентволуме, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentVolume`Свойство получает номер тома для текущего корневого каталога.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее текущий том DVD. Если диск входит в состав набора из нескольких томов, то целочисленное значение должно быть больше нуля.

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**волумесаваилабле**](volumesavailable-property.md)
</dt> </dl>

 

 



