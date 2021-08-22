---
description: Метод Жетвидеосизе извлекает собственные измерения видео.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Метод Жетвидеосизе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21746242211357e9e58e825d8e217799953dd569e91765acabe11fc2252d17c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536594"
---
# <a name="getvideosize-method"></a>Метод Жетвидеосизе

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetVideoSize`Метод получает собственные измерения видео.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект [двдрект](dvdrect-object.md) , содержащий четыре свойства для чтения и записи: (сверху слева) x; (сверху слева) y, Width и Height. Свойства **x** и **y** имеют нулевое значение, а другие два свойства соответствуют ширине и высоте видеопрямоугольника, созданного на диске.

 

 



