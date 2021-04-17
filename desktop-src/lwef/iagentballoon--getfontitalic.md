---
title: Иажентбаллун Жетфонтиталик
description: Иажентбаллун Жетфонтиталик
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710085"
---
# <a name="iagentballoongetfontitalic"></a>Иажентбаллун:: Жетфонтиталик

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Указывает, является ли шрифт, используемый в выноске слова, курсивом.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*пбфонтиталик*
</dt> <dd>

Адрес значения, которое принимает значение **true** , если шрифт является курсивом, и **значение false** , если он не является курсивом.

</dd> </dl>

Стиль шрифта, используемый в подсказке к слову, определяется в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может переопределить параметры шрифта для всех символов на странице свойств Microsoft Agent.

 

 




