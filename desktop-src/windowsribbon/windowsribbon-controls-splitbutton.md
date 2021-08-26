---
title: Разворачивающаяся кнопка
description: Разворачивающаяся кнопка — это составной элемент управления, с помощью которого пользователь может выбрать значение по умолчанию, привязанное к основной кнопке, или выбрать из списка взаимоисключающих значений, отображаемых в раскрывающемся списке, привязанном к дополнительной кнопке.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066a2275c49ad8d6dd32dd8ce4fd3d89956f204c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473760"
---
# <a name="split-button"></a>Разворачивающаяся кнопка

Разворачивающаяся кнопка — это составной элемент управления, с помощью которого пользователь может выбрать значение по умолчанию, привязанное к основной кнопке, или выбрать из списка взаимоисключающих значений, отображаемых в раскрывающемся списке, привязанном к дополнительной кнопке.

-   [Введение](#introduction)
-   [Свойства разворачивающейся кнопки](#split-button-properties)
-   [Связанные темы](#related-topics)

## <a name="introduction"></a>Введение

Этот элемент управления полезен для предоставления тесно связанных элементов в случаях, когда доступно очевидное по умолчанию, а отдельные элементы могут быть представлены изображением, текстом или обоими.

На следующем снимке экрана показана кнопка разделения ленты.

![снимок экрана элемента управления SplitButton в образце ленты.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Свойства разворачивающейся кнопки

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "кнопка разворачивающейся кнопки".

Как правило, свойство разворачивающейся кнопки обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления "кнопка разворачивающейся кнопки".




| Ключ свойства | Примечания | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.<br /> Если все дочерние элементы отключены, платформа устанавливает для <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> значение false (0). В противном случае, если один или несколько дочерних элементов включены, UI_PKEY_Enabled имеет значение true (-1).<blockquote>[!Important]<br />Свойство <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> элемента управления "разворачивающаяся кнопка" должно быть недействительным после включения или отключения одного или нескольких дочерних элементов. Это гарантирует, что платформа запрашивает обновленное значение свойства и обновляет состояние элемента управления "разворачивающаяся кнопка" в пользовательском интерфейсе ленты.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Может обновляться только через недействительность. | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Элемент разметки SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>
