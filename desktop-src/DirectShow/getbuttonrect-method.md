---
description: Метод Жетбуттонрект извлекает прямоугольник для указанной кнопки в координатах окна.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Метод Жетбуттонрект
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139342"
---
# <a name="getbuttonrect-method"></a>Метод Жетбуттонрект

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetButtonRect`Метод получает прямоугольник для указанной кнопки в координатах окна.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*ибуттон*
</dt> <dd>

Указывает номер кнопки в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект [двдрект](dvdrect-object.md) , определяющий прямоугольник.

## <a name="remarks"></a>Комментарии

Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**буттонсаваилабле**](buttonsavailable-property.md)
</dt> <dt>

[**куррентбуттон**](currentbutton-property.md)
</dt> <dt>

[**активатебуттон**](activatebutton-method.md)
</dt> <dt>

[**селектандактиватебуттон**](selectandactivatebutton-method.md)
</dt> <dt>

[**селектатпоситион**](selectatposition-method.md)
</dt> </dl>

 

 



