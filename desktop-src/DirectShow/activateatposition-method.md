---
description: Метод Активатеатпоситион активирует кнопку меню в указанной позиции.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Метод Активатеатпоситион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fee8b81c10b010132d07ac4418f273be228595bab45e86ec03c7828d78ba74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873554"
---
# <a name="activateatposition-method"></a>Метод Активатеатпоситион

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

Метод Активатеатпоситион активирует кнопку меню в указанной позиции.

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*
</dt> <dd>

Задает координату x в виде целого числа.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*
</dt> <dd>

Задает координату y в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**буттонсаваилабле**](buttonsavailable-property.md)
</dt> <dt>

[**куррентбуттон**](currentbutton-property.md)
</dt> <dt>

[**жетбуттонатпоситион**](getbuttonatposition-method.md)
</dt> <dt>

[**жетбуттонрект**](getbuttonrect-method.md)
</dt> <dt>

[**селектандактиватебуттон**](selectandactivatebutton-method.md)
</dt> <dt>

[**селектатпоситион**](selectatposition-method.md)
</dt> </dl>

 

 



