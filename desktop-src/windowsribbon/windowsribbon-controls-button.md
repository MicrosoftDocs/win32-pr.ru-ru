---
title: (Платформа Windows лента)
description: Кнопка — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134879"
---
# <a name="button-windows-ribbon-framework"></a>(Платформа Windows лента)

Кнопка — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.

-   [Введение](#introduction)
-   [Свойства кнопки](#button-properties)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

На следующем снимке экрана представлены три примера элемента кнопки на ленте.

![снимок экрана элементов управления "Кнопка" на ленте Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a>Свойства кнопки

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Кнопка".

Как правило, свойство Button обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления "Кнопка".



| Ключ свойства                                                                                             | Примечания                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Пользовательский интерфейс \_ PKEY \_ включен](windowsribbon-reference-properties-uipkey-enabled.md)                               | Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [UI \_ PKEY \_ keytip](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [\_Метка PKEY пользовательского интерфейса \_](windowsribbon-reference-properties-uipkey-label.md)                                   | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ лабелдескриптион](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ ларжехигхконтрастимаже](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ ларжеимаже](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ смаллхигхконтрастимаже](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ смаллимаже](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ тултиптитле](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Может обновляться только через недействительность.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Элемент разметки кнопки**](windowsribbon-element-button.md)
</dt> </dl>

 

 
