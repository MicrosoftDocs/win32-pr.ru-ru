---
title: Кнопка "Справка"
description: Кнопка Справка — это элемент управления, который пользователь может щелкнуть для вывода справочной системы приложения.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 295b3c7feae2aecada128dadbccd093f654c6a6660a68f4790975aee060aaf61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933392"
---
# <a name="help-button"></a>Кнопка "Справка"

Кнопка Справка — это элемент управления, который пользователь может щелкнуть для вывода справочной системы приложения.

-   [Сведения](#details)
-   [Свойства кнопки "Справка"](#help-button-properties)
-   [Связанные темы](#related-topics)

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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Хелпбуттон, элемент**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 