---
description: Метод Селектандактиватебуттон выбирает и активирует указанную кнопку.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Метод Селектандактиватебуттон
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682208"
---
# <a name="selectandactivatebutton-method"></a>Метод Селектандактиватебуттон

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SelectAndActivateButton`Метод выбирает и активирует указанную кнопку.

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*ибуттон*
</dt> <dd>

Задает кнопку в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

Этот метод выделяет указанную кнопку и активирует ее автоматически.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**буттонсаваилабле**](buttonsavailable-property.md)
</dt> <dt>

[**куррентбуттон**](currentbutton-property.md)
</dt> <dt>

[**активатебуттон**](activatebutton-method.md)
</dt> <dt>

[**жетбуттонатпоситион**](getbuttonatposition-method.md)
</dt> <dt>

[**жетбуттонрект**](getbuttonrect-method.md)
</dt> <dt>

[**селектатпоситион**](selectatposition-method.md)
</dt> </dl>

 

 



