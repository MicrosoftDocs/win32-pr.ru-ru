---
description: Метод Жетбуттонатпоситион извлекает номер кнопки по заданным координатам без выбора или активации.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Метод Жетбуттонатпоситион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139343"
---
# <a name="getbuttonatposition-method"></a>Метод Жетбуттонатпоситион

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetButtonAtPosition`Метод получает номер кнопки по заданным координатам без выбора или активации.

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*
</dt> <dd>

Задает координату по оси x для указателя мыши в виде целого числа.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*
</dt> <dd>

Задает координату y указателя мыши в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, задающее кнопку, если она имеется, в указанной позиции.

## <a name="remarks"></a>Комментарии

Этот метод возвращает нуль, если в заданных координатах отсутствует кнопка. Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**активатебуттон**](activatebutton-method.md)
</dt> <dt>

[**буттонсаваилабле**](buttonsavailable-property.md)
</dt> <dt>

[**куррентбуттон**](currentbutton-property.md)
</dt> <dt>

[**жетбуттонрект**](getbuttonrect-method.md)
</dt> <dt>

[**селектандактиватебуттон**](selectandactivatebutton-method.md)
</dt> <dt>

[**селектатпоситион**](selectatposition-method.md)
</dt> </dl>

 

 



