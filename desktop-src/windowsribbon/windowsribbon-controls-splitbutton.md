---
title: Разворачивающаяся кнопка
description: Разворачивающаяся кнопка — это составной элемент управления, с помощью которого пользователь может выбрать значение по умолчанию, привязанное к основной кнопке, или выбрать из списка взаимоисключающих значений, отображаемых в раскрывающемся списке, привязанном к дополнительной кнопке.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105691688"
---
# <a name="split-button"></a>Разворачивающаяся кнопка

Разворачивающаяся кнопка — это составной элемент управления, с помощью которого пользователь может выбрать значение по умолчанию, привязанное к основной кнопке, или выбрать из списка взаимоисключающих значений, отображаемых в раскрывающемся списке, привязанном к дополнительной кнопке.

-   [Введение](#introduction)
-   [Свойства разворачивающейся кнопки](#split-button-properties)
-   [См. также](#related-topics)

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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ключ свойства</th>
<th>Примечания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.<br/> Если все дочерние элементы отключены, платформа устанавливает для <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> значение false (0). В противном случае, если один или несколько дочерних элементов включены, UI_PKEY_Enabled имеет значение true (-1).
<blockquote>
[!Important]<br />
Свойство <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> элемента управления "разворачивающаяся кнопка" должно быть недействительным после включения или отключения одного или нескольких дочерних элементов. Это гарантирует, что платформа запрашивает обновленное значение свойства и обновляет состояние элемента управления "разворачивающаяся кнопка" в пользовательском интерфейсе ленты.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Элемент разметки SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>