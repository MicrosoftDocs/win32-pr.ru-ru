---
description: Свойство Буттонсаваилабле извлекает общее число кнопок в текущем меню.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Буттонсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423018"
---
# <a name="buttonsavailable-property"></a>Буттонсаваилабле, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ButtonsAvailable`Свойство получает общее количество кнопок в текущем меню.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее количество кнопок.

## <a name="remarks"></a>Комментарии

Это свойство доступно только для чтения и не имеет значения по умолчанию. Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.

Вызовите этот метод, чтобы получить верхний предел диапазона допустимых номеров кнопок.

## <a name="see-also"></a>См. также раздел

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

 

 



