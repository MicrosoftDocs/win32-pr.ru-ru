---
title: группа (Windowsная платформа ленты)
description: Группа организует связанные команды и элементы управления на вкладке.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c153f8cd9d1fc0d2d2bdbaabab0b2e15e099e50d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467421"
---
# <a name="group-windows-ribbon-framework"></a>группа (Windowsная платформа ленты)

Группа организует связанные команды и элементы управления на [вкладке](windowsribbon-controls-tab.md).

-   [Сведения](#details)
-   [Свойства группы](#group-properties)
-   [Связанные темы](#related-topics)

## <a name="details"></a>Сведения

На следующем снимке экрана показан элемент управления "группа ленты".

![снимок экрана с выносками, отображающими группу.](images/controls/group.png)

## <a name="group-properties"></a>Свойства группы

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления группы.

Как правило, свойство группы обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления группы.




| Ключ свойства | Примечания | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Может обновляться только через недействительность.<blockquote>[!Note]<br />Платформа требует, чтобы значение <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> для элемента управления группы начиналось с буквы верхнего регистра Z. Если значение, предоставленное приложением в методе обратного вызова <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>иуикоммандхандлер:: упдатепроперти</strong></a> , не начинается с буквы Z, это значение игнорируется, и вместо этого создается значение платформы. Значением платформы является буква Z, за которой следует числовое значение, начинающееся с 1 и последовательно увеличивающееся при необходимости для последующих элементов управления группы (Z1, Z2,..., ЗКС).</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Может обновляться только через недействительность. | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Group, элемент**](windowsribbon-element-group.md)
</dt> </dl>

