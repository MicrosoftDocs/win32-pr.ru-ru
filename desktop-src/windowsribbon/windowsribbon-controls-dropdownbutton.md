---
title: Кнопка Drop-Down
description: Кнопка Drop-Down состоит из кнопки, при нажатии на которой отображается раскрывающийся список взаимоисключающих элементов.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887b5979d5536b255526789aa541a6f2d1b67d1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473520"
---
# <a name="drop-down-button"></a>Кнопка Drop-Down

Кнопка Drop-Down состоит из кнопки, при нажатии на которой отображается раскрывающийся список взаимоисключающих элементов.

-   [Сведения](#details)
-   [Свойства кнопки раскрывающегося списка](#drop-down-button-properties)
-   [Связанные темы](#related-topics)

## <a name="details"></a>Сведения

Этот элемент управления полезен для предоставления тесно связанных элементов в случаях, когда очевидное значение по умолчанию недоступно и когда отдельные элементы могут быть представлены изображением, текстом или обоими.

На следующем снимке экрана показана кнопка Drop-Down ленты в образце ленты.

![снимок экрана элемента управления DropDownButton в образце ленты.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a>Свойства кнопки Drop-Down

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "кнопка" Drop-Down.

Как правило, свойство кнопки Drop-Down обновляется в пользовательском интерфейсе Ribbon путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления "кнопка Drop-Down".




| Ключ свойства | Примечания | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.<br /> Если все дочерние элементы отключены, платформа устанавливает для <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> значение false (0). В противном случае, если один или несколько дочерних элементов включены, UI_PKEY_Enabled имеет значение true (-1).<blockquote>[!Important]<br />Свойство <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> элемента управления "кнопка Drop-Down" должно быть недействительным после включения или отключения одного или нескольких дочерних элементов. Это гарантирует, что платформа запрашивает обновленное значение свойства и обновляет состояние элемента управления кнопки Drop-Down в пользовательском интерфейсе ленты.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.<blockquote>[!Note]<br />Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Может обновляться только через недействительность. | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**DropDownButton, элемент разметки**](windowsribbon-element-dropdownbutton.md)
</dt> </dl>
