---
title: Иажентбаллун Жетфонтнаме
description: Иажентбаллун Жетфонтнаме
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411360"
---
# <a name="iagentballoongetfontname"></a>Иажентбаллун:: Жетфонтнаме

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




