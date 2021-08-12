---
description: Свойство Волумесаваилабле извлекает количество томов в наборе из нескольких томов.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Волумесаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ab5b07f30e49f1bbe7655a2d66d9aaa683099df64cadf94b5dfffdd3b3af0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650941"
---
# <a name="volumesavailable-property"></a>Волумесаваилабле, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`VolumesAvailable`Свойство получает количество томов в многотомном наборе.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество томов в наборе в виде целого числа.

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию. Некоторые заголовки DVD могут быть выпущены в виде набора или ряда с несколькими дисками. Используйте этот метод, чтобы определить номер тома для текущего диска.

 

 



