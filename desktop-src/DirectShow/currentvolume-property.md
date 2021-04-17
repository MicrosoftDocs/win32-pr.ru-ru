---
description: Свойство Куррентволуме извлекает номер тома для текущего корневого каталога.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Куррентволуме, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672961"
---
# <a name="currentvolume-property"></a>Куррентволуме, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentVolume`Свойство получает номер тома для текущего корневого каталога.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее текущий том DVD. Если диск входит в состав набора из нескольких томов, то целочисленное значение должно быть больше нуля.

## <a name="remarks"></a>Комментарии

Это свойство доступно только для чтения и не имеет значения по умолчанию.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**волумесаваилабле**](volumesavailable-property.md)
</dt> </dl>

 

 



