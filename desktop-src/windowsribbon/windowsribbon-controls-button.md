---
title: кнопка (платформа ленты Windows)
description: Кнопка — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82a1a71181b3478e065922b5a1836f6cd0f47bf9b3f2e497f45564118449b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707801"
---
# <a name="button-windows-ribbon-framework"></a>кнопка (платформа ленты Windows)

Кнопка — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.

-   [Введение](#introduction)
-   [Свойства кнопки](#button-properties)
-   [Связанные темы](#related-topics)

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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Элемент разметки кнопки**](windowsribbon-element-button.md)
</dt> </dl>

 

 
