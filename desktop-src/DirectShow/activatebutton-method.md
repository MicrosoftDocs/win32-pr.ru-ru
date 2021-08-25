---
description: Метод Активатебуттон активирует выбранную кнопку меню.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Метод Активатебуттон
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64853a191f688758deb42061e95c91308ff88c00fe9482cce677f8b00926f26f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873524"
---
# <a name="activatebutton-method"></a>Метод Активатебуттон

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

Метод Активатебуттон активирует выбранную кнопку меню.

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

Этот метод используется для активации кнопки, выбранной с помощью метода [**селектлефтбуттон**](selectleftbutton-method.md), [**селектловербуттон**](selectlowerbutton-method.md), [**селектуппербуттон**](selectupperbutton-method.md)или [**селектригхтбуттон**](selectrightbutton-method.md) .

 

 



