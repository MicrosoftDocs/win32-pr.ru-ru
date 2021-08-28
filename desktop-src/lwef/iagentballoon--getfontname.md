---
title: Иажентбаллун Жетфонтнаме
description: Иажентбаллун Жетфонтнаме
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb0bceae040f9261d2530b19d074df937dbdaf80d91a27f57b5cf9c1fd8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725326"
---
# <a name="iagentballoongetfontname"></a>Иажентбаллун:: Жетфонтнаме

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Извлекает значение шрифта, отображаемого в тексте всплывающей подсказки.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*пбсзфонтнаме*
</dt> <dd>

Адрес объекта BSTR, который получает имя шрифта, отображаемое в тексте всплывающей подсказки.

</dd> </dl>

Шрифт по умолчанию, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent. Его можно изменить с помощью [**иажентбаллун:: сетфонтнаме**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**). Пользователь может переопределить параметр шрифта для всех символов с помощью страницы свойств Microsoft Agent.

 

 




