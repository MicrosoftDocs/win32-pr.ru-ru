---
title: Элемент управления автоradiobutton
description: Определяет автоматический элемент управления "переключатель". Этот элемент управления автоматически выполняет взаимное исключение с другими элементами управления "автоradiobutton" в той же группе. Когда эта кнопка выбрана, приложение получает извещение о \_ нажатии млрд долл.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Меню элемента управления автоradiobutton и другие ресурсы
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783888"
---
# <a name="autoradiobutton-control"></a>Элемент управления автоradiobutton

Определяет автоматический элемент управления "переключатель". Этот элемент управления автоматически выполняет взаимное исключение с другими элементами управления " **автоradiobutton** " в той же группе. Когда эта кнопка выбрана, приложение получает извещение о **\_ нажатии млрд долл**.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*полнотекстовым*
</dt> <dd>

Текст, который будет отображаться рядом с переключателем.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили для автоматического переключателя, которые могут быть сочетанием стилей классов кнопок и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.

Если стиль не указан, используется стиль по умолчанию `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[Переключатели](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




