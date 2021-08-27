---
title: Коллекция In-Ribbon
description: Коллекция In-Ribbon — это элемент управления, отображающий коллекцию связанных элементов или команд на ленте. Если в коллекции слишком много элементов, для показа остальной части коллекции в развернутой области предоставляется стрелка развертывания.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713455e962996e2cc1a70b418000d0f94a383174
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479800"
---
# <a name="in-ribbon-gallery"></a>Коллекция In-Ribbon

Коллекция In-Ribbon — это элемент управления, отображающий коллекцию связанных элементов или команд на ленте. Если в коллекции слишком много элементов, для показа остальной части коллекции в развернутой области предоставляется стрелка развертывания.

-   [Сведения](#details)
-   [Свойства коллекции на ленте](#in-ribbon-gallery-properties)
-   [Связанные темы](#related-topics)

## <a name="details"></a>Сведения

На следующем снимке экрана показан элемент управления "Коллекция" ленты In-Ribbon в Microsoft Paint.

![снимок экрана элемента управления инриббонгаллери на ленте Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a>Свойства коллекции In-Ribbon

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления коллекции In-Ribbon.

Как правило, свойство коллекции In-Ribbon обновляется в пользовательском интерфейсе Ribbon путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления "коллекция In-Ribbon".




| Ключ свойства | Примечания | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(допустимо только для коллекции элементов)<br /> | Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.<blockquote>[!Note]<br />Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Может обновляться только через недействительность. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Может обновляться только через недействительность. | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Инриббонгаллери, элемент**](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> <dt>

[Пример коллекции](windowsribbon-gallerysample.md)
</dt> </dl>

