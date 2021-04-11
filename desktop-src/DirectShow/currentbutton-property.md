---
description: Свойство Куррентбуттон извлекает номер выбранной кнопки меню.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Куррентбуттон, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341862"
---
# <a name="currentbutton-property"></a>Куррентбуттон, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentButton`Свойство получает номер выбранной кнопки меню.

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее кнопку.

## <a name="remarks"></a>Комментарии

Это свойство доступно только для чтения и не имеет значения по умолчанию. Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**активатебуттон**](activatebutton-method.md)
</dt> <dt>

[**буттонсаваилабле**](buttonsavailable-property.md)
</dt> <dt>

[**жетбуттонатпоситион**](getbuttonatposition-method.md)
</dt> <dt>

[**жетбуттонрект**](getbuttonrect-method.md)
</dt> <dt>

[**селектандактиватебуттон**](selectandactivatebutton-method.md)
</dt> <dt>

[**селектатпоситион**](selectatposition-method.md)
</dt> </dl>

 

 



