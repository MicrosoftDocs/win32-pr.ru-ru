---
title: UI_PKEY_FontProperties_DeltaSize
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ делтасизе.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070020"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>UI \_ PKEY \_ фонтпропертиес \_ делтасизе

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ делтасизе.

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ делтасизе используется приложением в случаях, когда невозможно указать для приложения значение **размера шрифта**, например, если выбрано выполнение хетероженеаусли размера текста. Элемент управления " **Размер шрифта** " имеет значение "пустой", а UI \_ PKEY \_ фонтпропертиес \_ делтасизе используется для записи взаимодействия пользователя с кнопками " **увеличение шрифта** " и " **Сжатие шрифта** ".

UI \_ PKEY \_ фонтпропертиес \_ Делтасизе входит в [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

На следующем снимке экрана показаны кнопки **увеличение размера шрифта** и **Сжатие шрифта** на ленте [**фонтконтрол**](windowsribbon-element-fontcontrol.md).

![снимок экрана с кнопками увеличения и уменьшения размера шрифта в фонтконтрол.](images/markup/fontcontrol-incdec.png)

В следующей таблице описаны значения свойств.



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | Нажата кнопка " **увеличить шрифт** ".   |
| `UI_FONTDELTASIZE_SHRINK` | Нажата кнопка " **Сжать шрифт** ". |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтделтасизе пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 