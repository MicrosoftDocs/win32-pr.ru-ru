---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259056"
---
# <a name="iagentballoongetfontsize"></a>Иажентбаллун:: FontSize

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




