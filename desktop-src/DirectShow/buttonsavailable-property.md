---
description: Свойство Буттонсаваилабле извлекает общее число кнопок в текущем меню.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Буттонсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16e14675238711ef0b572477334fecba0311ca2bb54d67fc3fe012ae6d1ede9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955563"
---
# <a name="buttonsavailable-property"></a>Буттонсаваилабле, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ButtonsAvailable`Свойство получает общее количество кнопок в текущем меню.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее количество кнопок.

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию. Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

Вызовите этот метод, чтобы получить верхний предел диапазона допустимых номеров кнопок.

## <a name="see-also"></a>См. также

<dl> <dt>

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

 

 



