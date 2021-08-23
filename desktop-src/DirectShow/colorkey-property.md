---
description: Свойство ColorKey задает или получает цветовой ключ, используемый в закрытых субтитрах.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: ColorKey, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abca1dabbdb67f4380dbe32acbf2948862695b7c424dfd08629ec16237bb88c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073738"
---
# <a name="colorkey-property"></a>ColorKey, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ColorKey`Свойство задает или получает цветовой ключ, используемый в закрытых субтитрах.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее цвет, используемый в качестве прозрачного фона для текста с субтитрами. Значение по умолчанию в 256 Colors — пурпурный, а «выкл.-черный» — в любой другой глубине цвета.

## <a name="remarks"></a>Remarks

Это свойство доступно для чтения и записи. Это свойство применяется только к закрытым заголовкам, если таковые существуют, а не к потоку субтитров.

 

 



