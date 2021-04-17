---
description: Метод Жетвидеосизе извлекает собственные измерения видео.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Метод Жетвидеосизе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673103"
---
# <a name="getvideosize-method"></a>Метод Жетвидеосизе

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetVideoSize`Метод получает собственные измерения видео.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект [двдрект](dvdrect-object.md) , содержащий четыре свойства для чтения и записи: (сверху слева) x; (сверху слева) y, Width и Height. Свойства **x** и **y** имеют нулевое значение, а другие два свойства соответствуют ширине и высоте видеопрямоугольника, созданного на диске.

 

 



