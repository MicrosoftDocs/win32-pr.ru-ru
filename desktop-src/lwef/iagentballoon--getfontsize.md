---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc392bd12fccfb01b8aee41a5a06ed50b388ac8223e622d75218c840f706c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962494"
---
# <a name="iagentballoongetfontsize"></a>Иажентбаллун:: FontSize

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Извлекает значение размера шрифта, отображаемого в подсказке к слову.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*плфонтсизе*
</dt> <dd>

Адрес значения, получающего размер шрифта.

</dd> </dl>

Размер шрифта по умолчанию, используемый в подсказке для символьного слова, определяется в редакторе символов Microsoft Agent. Его можно изменить с помощью [**иажентбаллун:: сетфонтсизе**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). Однако пользователь может переопределить параметры размера шрифта для всех символов с помощью страницы свойств Microsoft Agent.

 

 




