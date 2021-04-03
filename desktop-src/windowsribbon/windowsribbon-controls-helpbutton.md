---
title: Кнопка "Справка"
description: Кнопка Справка — это элемент управления, который пользователь может щелкнуть для вывода справочной системы приложения.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987528"
---
# <a name="help-button"></a>Кнопка "Справка"

Кнопка Справка — это элемент управления, который пользователь может щелкнуть для вывода справочной системы приложения.

-   [Подробные сведения](#details)
-   [Свойства кнопки "Справка"](#help-button-properties)
-   [См. также](#related-topics)

## <a name="details"></a>Сведения

На следующем снимке экрана показана кнопка Справка на ленте.

![снимок экрана с кнопкой "Справка".](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Свойства кнопки "Справка"

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления кнопки "Справка".

Как правило, свойство кнопки справки обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления кнопки "Справка".



| Ключ свойства                                                                                     | Примечания                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ keytip](windowsribbon-reference-properties-uipkey-keytip.md)                         | Может обновляться только через недействительность. |
| [\_Метка PKEY пользовательского интерфейса \_](windowsribbon-reference-properties-uipkey-label.md)                           | Может обновляться только через недействительность. |
| [UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Может обновляться только через недействительность. |
| [UI \_ PKEY \_ тултиптитле](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Может обновляться только через недействительность. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Хелпбуттон, элемент**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 